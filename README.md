/*
# Caixa-de-banco
Cria uma lista de senhas para serem requisitadas pelos 4 caixas operacionais. Caixa 1 retira primeiro as senhas prioritárias, caixa 2 e 3 retiram primeiro as senhas rápidas, e o caixa 4 retira primeiro as senhas comuns.
*/

package mapa_ii;

/**
 * @author Walyson
 */
 
public class Principal {

    private int numero;
    private String tipo;
    
    public Principal(int numero, String tipo){
        this.numero = numero;
        this.tipo = tipo;
    }
    
    public Principal(){
        this.numero = 0;
        this.tipo = "";
    }

    public int getNumero() {
        return numero;
    }

    public void setNumero(int numero) {
        this.numero = numero;
    }

    public String getTipo() {
        return tipo;
    }

    public void setTipo(String tipo) {
        this.tipo = tipo;
    }
    
}
////////////////////////////////////////////////////////////////
//INTERFACE


package mapa_ii;

import java.util.ArrayList;
import java.util.ConcurrentModificationException;
import java.util.List;
import java.util.Iterator;

/**
 * @author Walyson
 */
 
public class Interface_Banco extends javax.swing.JFrame {

    
    List<Principal> listaSenha;
    int numero;
    /*
    String C = "C";
    String P = "P";
    String R = "R";
    */
    public Interface_Banco() {
        initComponents();
        numero = 0;
        listaSenha = new ArrayList<Principal>();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {
        bindingGroup = new org.jdesktop.beansbinding.BindingGroup();

        pCliente = new javax.swing.JPanel();
        jLabel1 = new javax.swing.JLabel();
        bComum = new javax.swing.JButton();
        bRapido = new javax.swing.JButton();
        bPrioritario = new javax.swing.JButton();
        jLabel2 = new javax.swing.JLabel();
        tfSenhaCliente = new javax.swing.JTextField();
        pCaixa = new javax.swing.JPanel();
        bCaixa1 = new javax.swing.JButton();
        bCaixa2 = new javax.swing.JButton();
        bCaixa3 = new javax.swing.JButton();
        bCaixa4 = new javax.swing.JButton();
        labelParaClientes = new javax.swing.JLabel();
        labelParaCaixa = new javax.swing.JLabel();
        tfSenhaTela = new javax.swing.JTextField();
        tfCaixa = new javax.swing.JTextField();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);
        setBackground(new java.awt.Color(220, 220, 220));

        pCliente.setBorder(javax.swing.BorderFactory.createBevelBorder(javax.swing.border.BevelBorder.LOWERED));
        pCliente.setForeground(new java.awt.Color(220, 220, 220));
        pCliente.setFont(new java.awt.Font("Arial", 0, 12)); // NOI18N

        jLabel1.setFont(new java.awt.Font("Arial", 0, 14)); // NOI18N
        jLabel1.setText("Escolha seu tipo de atendimento:");

        bComum.setFont(new java.awt.Font("Arial", 0, 12)); // NOI18N
        bComum.setText("Comum");

        org.jdesktop.beansbinding.Binding binding = org.jdesktop.beansbinding.Bindings.createAutoBinding(org.jdesktop.beansbinding.AutoBinding.UpdateStrategy.READ_WRITE, tfSenhaCliente, org.jdesktop.beansbinding.ELProperty.create("${text_ON_ACTION_OR_FOCUS_LOST}"), bComum, org.jdesktop.beansbinding.BeanProperty.create("actionCommand"));
        bindingGroup.addBinding(binding);

        bComum.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bComumActionPerformed(evt);
            }
        });

        bRapido.setFont(new java.awt.Font("Arial", 0, 12)); // NOI18N
        bRapido.setText("Rápido");
        bRapido.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bRapidoActionPerformed(evt);
            }
        });

        bPrioritario.setFont(new java.awt.Font("Arial", 0, 12)); // NOI18N
        bPrioritario.setText("Prioritário");
        bPrioritario.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bPrioritarioActionPerformed(evt);
            }
        });

        jLabel2.setFont(new java.awt.Font("Arial", 0, 12)); // NOI18N
        jLabel2.setText("Sua senha é:");

        tfSenhaCliente.setFont(new java.awt.Font("Arial", 0, 14)); // NOI18N
        tfSenhaCliente.setHorizontalAlignment(javax.swing.JTextField.CENTER);
        tfSenhaCliente.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                tfSenhaClienteActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout pClienteLayout = new javax.swing.GroupLayout(pCliente);
        pCliente.setLayout(pClienteLayout);
        pClienteLayout.setHorizontalGroup(
            pClienteLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, pClienteLayout.createSequentialGroup()
                .addContainerGap(11, Short.MAX_VALUE)
                .addComponent(jLabel1)
                .addGap(127, 127, 127))
            .addGroup(pClienteLayout.createSequentialGroup()
                .addGap(28, 28, 28)
                .addGroup(pClienteLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(pClienteLayout.createSequentialGroup()
                        .addComponent(tfSenhaCliente, javax.swing.GroupLayout.PREFERRED_SIZE, 292, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(0, 0, Short.MAX_VALUE))
                    .addGroup(pClienteLayout.createSequentialGroup()
                        .addComponent(bComum, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addGap(28, 28, 28)
                        .addGroup(pClienteLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addGroup(pClienteLayout.createSequentialGroup()
                                .addComponent(jLabel2)
                                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                            .addGroup(pClienteLayout.createSequentialGroup()
                                .addComponent(bRapido, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                                .addGap(28, 28, 28)
                                .addComponent(bPrioritario, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                                .addGap(28, 28, 28))))))
        );
        pClienteLayout.setVerticalGroup(
            pClienteLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(pClienteLayout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jLabel1)
                .addGap(18, 18, 18)
                .addGroup(pClienteLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(bComum)
                    .addComponent(bRapido)
                    .addComponent(bPrioritario))
                .addGap(34, 34, 34)
                .addComponent(jLabel2)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addComponent(tfSenhaCliente, javax.swing.GroupLayout.DEFAULT_SIZE, 30, Short.MAX_VALUE)
                .addContainerGap())
        );

        pCaixa.setBorder(javax.swing.BorderFactory.createBevelBorder(javax.swing.border.BevelBorder.LOWERED));
        pCaixa.setForeground(new java.awt.Color(220, 220, 220));

        bCaixa1.setFont(new java.awt.Font("Arial", 0, 24)); // NOI18N
        bCaixa1.setText("Caixa 1");
        bCaixa1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bCaixa1ActionPerformed(evt);
            }
        });

        bCaixa2.setFont(new java.awt.Font("Arial", 0, 24)); // NOI18N
        bCaixa2.setText("Caixa 2");
        bCaixa2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bCaixa2ActionPerformed(evt);
            }
        });

        bCaixa3.setFont(new java.awt.Font("Arial", 0, 24)); // NOI18N
        bCaixa3.setText("Caixa 3");
        bCaixa3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bCaixa3ActionPerformed(evt);
            }
        });

        bCaixa4.setFont(new java.awt.Font("Arial", 0, 24)); // NOI18N
        bCaixa4.setText("Caixa 4");
        bCaixa4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                bCaixa4ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout pCaixaLayout = new javax.swing.GroupLayout(pCaixa);
        pCaixa.setLayout(pCaixaLayout);
        pCaixaLayout.setHorizontalGroup(
            pCaixaLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(pCaixaLayout.createSequentialGroup()
                .addGroup(pCaixaLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(pCaixaLayout.createSequentialGroup()
                        .addGap(0, 11, Short.MAX_VALUE)
                        .addComponent(bCaixa1)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 16, Short.MAX_VALUE)
                        .addComponent(bCaixa2))
                    .addGroup(pCaixaLayout.createSequentialGroup()
                        .addGap(0, 0, Short.MAX_VALUE)
                        .addComponent(bCaixa3)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(bCaixa4)))
                .addContainerGap())
        );
        pCaixaLayout.setVerticalGroup(
            pCaixaLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(pCaixaLayout.createSequentialGroup()
                .addGap(36, 36, 36)
                .addGroup(pCaixaLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(bCaixa1)
                    .addComponent(bCaixa2))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addGroup(pCaixaLayout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(bCaixa3)
                    .addComponent(bCaixa4))
                .addGap(26, 26, 26))
        );

        labelParaClientes.setFont(new java.awt.Font("Arial", 0, 18)); // NOI18N
        labelParaClientes.setText("Para clientes:");

        labelParaCaixa.setFont(new java.awt.Font("Arial", 0, 18)); // NOI18N
        labelParaCaixa.setText("Para caixas:");

        tfSenhaTela.setBackground(new java.awt.Color(220, 220, 220));
        tfSenhaTela.setFont(new java.awt.Font("Arial", 1, 36)); // NOI18N
        tfSenhaTela.setHorizontalAlignment(javax.swing.JTextField.CENTER);
        tfSenhaTela.setBorder(null);

        tfCaixa.setBackground(new java.awt.Color(220, 220, 220));
        tfCaixa.setFont(new java.awt.Font("Arial", 0, 18)); // NOI18N
        tfCaixa.setHorizontalAlignment(javax.swing.JTextField.CENTER);
        tfCaixa.setBorder(null);

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addContainerGap()
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addComponent(labelParaClientes)
                            .addComponent(pCliente, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addGap(18, 18, Short.MAX_VALUE)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addComponent(labelParaCaixa)
                            .addComponent(pCaixa, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(247, 247, 247)
                        .addComponent(tfSenhaTela, javax.swing.GroupLayout.PREFERRED_SIZE, 156, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(0, 0, Short.MAX_VALUE)))
                .addContainerGap())
            .addGroup(layout.createSequentialGroup()
                .addGap(269, 269, 269)
                .addComponent(tfCaixa, javax.swing.GroupLayout.PREFERRED_SIZE, 106, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addGap(62, 62, 62)
                .addComponent(tfSenhaTela, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(18, 18, 18)
                .addComponent(tfCaixa, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 73, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(labelParaClientes)
                    .addComponent(labelParaCaixa))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING, false)
                    .addComponent(pCaixa, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(pCliente, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addContainerGap())
        );

        bindingGroup.bind();

        pack();
    }// </editor-fold>                        

    private void bComumActionPerformed(java.awt.event.ActionEvent evt) {                                       
        numero++;
        
        Principal senhaCliente = new Principal(numero, "C");
        listaSenha.add(senhaCliente);
        tfSenhaCliente.setText(String.valueOf(senhaCliente.getTipo()) + "-" + 
                String.valueOf(senhaCliente.getNumero()));
        
    }                                      

    private void tfSenhaClienteActionPerformed(java.awt.event.ActionEvent evt) {                                               
        
    }                                              

    private void bRapidoActionPerformed(java.awt.event.ActionEvent evt) {                                        
        numero++;
        
        Principal senhaCliente = new Principal(numero, "R");
        listaSenha.add(senhaCliente);
        tfSenhaCliente.setText(String.valueOf(senhaCliente.getTipo()) + "-" + 
                String.valueOf(senhaCliente.getNumero()));
    }                                       

    private void bPrioritarioActionPerformed(java.awt.event.ActionEvent evt) {                                             
        numero++;
        
        Principal senhaCliente = new Principal(numero, "P");
        listaSenha.add(senhaCliente);
        tfSenhaCliente.setText(String.valueOf(senhaCliente.getTipo()) + "-" + 
                String.valueOf(senhaCliente.getNumero()));
    }                                            

    private void bCaixa1ActionPerformed(java.awt.event.ActionEvent evt) {                                        
        Iterator<Principal> itr = listaSenha.iterator();
        
        
        while(itr.hasNext()){
            
            for(Principal p : listaSenha){
                
                if(p.getTipo().contains("P")){
                    
                    listaSenha.remove(p);
                    tfCaixa.setText("Caixa 1");
                    tfSenhaTela.setText(String.valueOf(p.getTipo()) + "-" + 
                        String.valueOf(p.getNumero()));
                    break;
                }
                
            }
            
            try{
                Principal senha = itr.next();
                itr.remove();
                tfCaixa.setText("Caixa 1");
                tfSenhaTela.setText(String.valueOf(senha.getTipo()) + "-" + 
                    String.valueOf(senha.getNumero()));
            }catch(ConcurrentModificationException e){
            }
            
            
            break;
        }
        
        
    }                                       

    private void bCaixa2ActionPerformed(java.awt.event.ActionEvent evt) {                                        
        Iterator<Principal> itr = listaSenha.iterator();
        
        while(itr.hasNext()){
            
            for(Principal p : listaSenha){
                
                if(p.getTipo().contains("R")){
                    
                    listaSenha.remove(p);
                    tfCaixa.setText("Caixa 2");
                    tfSenhaTela.setText(String.valueOf(p.getTipo()) + "-" + 
                        String.valueOf(p.getNumero()));
                    break;
                }
                
            }
            
            try{
                Principal senha = itr.next();
                itr.remove();
                tfCaixa.setText("Caixa 2");
                tfSenhaTela.setText(String.valueOf(senha.getTipo()) + "-" + 
                    String.valueOf(senha.getNumero()));
            }catch(ConcurrentModificationException e){
            }
            
            break;
        }
        
    }                                       

    private void bCaixa3ActionPerformed(java.awt.event.ActionEvent evt) {                                        
        Iterator<Principal> itr = listaSenha.iterator();
        
        while(itr.hasNext()){
            
            for(Principal p : listaSenha){
                
                if(p.getTipo().contains("R")){
                    
                    listaSenha.remove(p);
                    tfCaixa.setText("Caixa 3");
                    tfSenhaTela.setText(String.valueOf(p.getTipo()) + "-" + 
                        String.valueOf(p.getNumero()));
                    break;
                }
                
            }
            
            try{
                Principal senha = itr.next();
                itr.remove();
                tfCaixa.setText("Caixa 3");
                tfSenhaTela.setText(String.valueOf(senha.getTipo()) + "-" + 
                    String.valueOf(senha.getNumero()));
            }catch(ConcurrentModificationException e){
            }
            
            break;
        }
        
        
    }                                       

    private void bCaixa4ActionPerformed(java.awt.event.ActionEvent evt) {                                        
        Iterator<Principal> itr = listaSenha.iterator();
        
        while(itr.hasNext()){
            
            for(Principal p : listaSenha){
                
                if(p.getTipo().contains("C")){
                    
                    listaSenha.remove(p);
                    tfCaixa.setText("Caixa 4");
                    tfSenhaTela.setText(String.valueOf(p.getTipo()) + "-" + 
                        String.valueOf(p.getNumero()));
                    break;
                }
                
            }
            
            try{
                Principal senha = itr.next();
                itr.remove();
                tfCaixa.setText("Caixa 4");
                tfSenhaTela.setText(String.valueOf(senha.getTipo()) + "-" + 
                    String.valueOf(senha.getNumero()));
            }catch(ConcurrentModificationException e){
            }
            
            break;
        }
        
    }                                       

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(Interface_Banco.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(Interface_Banco.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(Interface_Banco.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(Interface_Banco.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new Interface_Banco().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton bCaixa1;
    private javax.swing.JButton bCaixa2;
    private javax.swing.JButton bCaixa3;
    private javax.swing.JButton bCaixa4;
    private javax.swing.JButton bComum;
    private javax.swing.JButton bPrioritario;
    private javax.swing.JButton bRapido;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel labelParaCaixa;
    private javax.swing.JLabel labelParaClientes;
    private javax.swing.JPanel pCaixa;
    private javax.swing.JPanel pCliente;
    private javax.swing.JTextField tfCaixa;
    private javax.swing.JTextField tfSenhaCliente;
    private javax.swing.JTextField tfSenhaTela;
    private org.jdesktop.beansbinding.BindingGroup bindingGroup;
    // End of variables declaration                   
}
