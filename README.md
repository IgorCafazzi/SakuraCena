# SakuraCena
## Drivers

https://drive.google.com/file/d/1u6rPod_F6wE6SD_REvnsrNTeDvp8J40V/view?usp=sharing

https://drive.google.com/drive/folders/1bJkUfEf_iZcZciaTlV0IrVESCSezpKnW?hl=pt-br



____

vídeo barra hp: https://youtu.be/BLfNP4Sc_iA?si=PhstaMnW1TIv8wjy

assets casas: https://assetstore.unity.com/packages/3d/environments/urban/town-houses-pack-42717

asset rua: https://assetstore.unity.com/packages/3d/small-town-america-streets-free-59759

skybox: https://assetstore.unity.com/packages/2d/textures-materials/sky/allsky-free-10-sky-skybox-set-146014

low poly avenida: https://assetstore.unity.com/packages/3d/environments/boki-low-poly-nature-206385

low poly casas: https://assetstore.unity.com/packages/3d/props/exterior/low-poly-houses-free-pack-243926

florestas: https://assetstore.unity.com/packages/3d/vegetation/lowpoly-forest-lite-291277  https://assetstore.unity.com/packages/3d/vegetation/environment-pack-free-forest-sample-168396  https://assetstore.unity.com/packages/3d/environments/landscapes/free-low-poly-nature-forest-205742

script para troca de cena ao clicar no botão (menu): 

![image](https://github.com/user-attachments/assets/fd376fed-d736-43b3-8560-4805ac41a5f4)

script para sair do jogo: 

![image](https://github.com/user-attachments/assets/6b2a4ce5-a05d-48b2-8e8b-662fe4268cb3)


script movimentação (talvez só referência): 

![image](https://github.com/user-attachments/assets/a165a777-ed44-4c69-829a-c3668f433a2c)


script patrulha boss: 

![image](https://github.com/user-attachments/assets/c31b47fa-cb72-4f8a-b5b5-c199ffcab46a)


script caixa de dialogo:

![image](https://github.com/user-attachments/assets/f03bd498-546b-44e5-8fa1-f8edcb3f8c0b)

barra de vida script:

![image](https://github.com/user-attachments/assets/778aa7e9-17a0-4e35-ae63-0fc96e31cde4)
![image](https://github.com/user-attachments/assets/5a311854-6b35-4eef-a377-fffcfb6fcc19)

using UnityEngine;

public class TransformacaoPersonagem : MonoBehaviour
{
    // Prefabs dos dois estados do personagem
    public GameObject formaInicial;
    public GameObject formaTransformada;

    // Define o estado inicial
    private bool estaTransformado = false;

    void Start()
    {
        // Ativa a forma inicial e desativa a transformada no início
        formaInicial.SetActive(true);
        formaTransformada.SetActive(false);
    }

    void Update()
    {
        // Verifica se a tecla T foi pressionada
        if (Input.GetKeyDown(KeyCode.T))
        {
            AlternarForma();
        }
    }

    void AlternarForma()
    {
        // Alterna entre as formas
        estaTransformado = !estaTransformado;

        formaInicial.SetActive(!estaTransformado);
        formaTransformada.SetActive(estaTransformado);
    }
}

script menu

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Menu : MonoBehaviour
{
    public void PlayGame()
    {
        SceneManager.LoadSceneAsync(1);
    }

    public void QuitGame()
    {
        Application.Quit();
    }
}
