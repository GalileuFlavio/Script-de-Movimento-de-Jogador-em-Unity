# Script-de-Movimento-de-Jogador-em-Unity
Um script simples que permite o movimento do jogador em um ambiente 2D ou 3D na Unity.

using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float speed = 5f;

    void Update()
    {
        float horizontalInput = Input.GetAxis("Horizontal");
        float verticalInput = Input.GetAxis("Vertical");

        Vector3 movement = new Vector3(horizontalInput, 0f, verticalInput);
        transform.Translate(movement * speed * Time.deltaTime);
    }
}
