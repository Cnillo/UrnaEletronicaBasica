codico fonte

package com.mycompany.atividade1;

import javax.swing.JOptionPane;

/**
 *
 * @author NILLO
 */
public class Atividade1 {

    public static void main(String[] args) {
        
        int eleitores = 0;
        int rep = 0;
        int voto = 0;
        int ze = 0;
        int rita= 0;
        int porcentagem = 0;
        int porcentagem2 = 0;
        
        String eleitoresstr = JOptionPane.showInputDialog(null, "digite a quantidade de eleitores");
        eleitores = Integer.parseInt(eleitoresstr);
        System.out.println("n° eleitores é " + eleitores);
 
            while(rep < eleitores){
            String votostr = JOptionPane.showInputDialog(null, "digite 1 para zé da farmacia ou digite 2 para rita da padaria");
            voto = Integer.parseInt(votostr);
            
            if(voto == 1 ){
                System.out.println("voce votou no ze da farmacia");
                rep++;
                ze++;
                }else if(voto ==2){
                System.out.println("voce votou na rita da padaria");
                rep++;
                rita++;
                }else{
                JOptionPane.showMessageDialog(null, "digite um valor valido");
                System.out.println("foi digitado um valor invalido não contabilizado");
                }
            
            }
            porcentagem = (ze * 100) / eleitores;
            porcentagem2 = (rita * 100) / eleitores;
            JOptionPane.showMessageDialog(null, "o total de eleitores foi " + eleitores + "\n" +
             "ze da farmacia teve " + ze + " votos equivalente a " + porcentagem + " %" + "\n" +
             "rita da padaria teve " + rita + " votos equivalente a " + porcentagem2 + " %");
            
    }
}
