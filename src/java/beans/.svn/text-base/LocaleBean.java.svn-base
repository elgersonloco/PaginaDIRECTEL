package beans;
/*=================================================================================================================                                          
         QUAD-TREE
         ============================
                                 
         DESCRIPTION
         ==============================
             Maneja El cambio de Lenguaje y Locale del Proyecto
                                                                                                    
                 
         PROGRAMMING RECORD
         =============================

          DATE             MODIFIED BY                           DESCRIPTION 
         =============    ===================================   =====================================================              
         Apr 19th 2013    Gerardo Hdz. Juan Francisco(Howser)    Creación del Bean
              
=====================================================================================================================*/
import com.sun.faces.taglib.html_basic.CommandLinkTag;
import java.util.Locale;

import javax.faces.bean.ManagedBean;
import javax.faces.bean.SessionScoped;
import javax.faces.component.UIComponent;
import javax.faces.context.FacesContext;

@ManagedBean
@SessionScoped
public class LocaleBean {

    private Locale locale = FacesContext.getCurrentInstance().getViewRoot().getLocale();

    public Locale getLocale() {
        return locale;
    }

    public String getLanguage() {
        return locale.getLanguage();
    }

    public void setLanguage(String language) {
        locale = new Locale(language);
        FacesContext.getCurrentInstance().getViewRoot().setLocale(locale);
    }

    /**
     * changeLang : Cambia el Locale y Lenguaje a uno determinado
     * 
     * @since: April 20th, 2013
     * @param language : Idioma al que se quiere Cambiar
     * @return String null
     */
    public String changeLang(String language) {
        //Nuevo Locale y Lang
        locale = new Locale(language);
        FacesContext.getCurrentInstance().getViewRoot().setLocale(locale);
        
        return null;
    }//changeLang
    
    /**
     * setStyle : Determina si un Lenguaje esta siendo usado e indica el estilo a aplicar
     * 
     * @since: April 20th, 2013
     * @param language
     * @return String - estilo a aplicar
     */
    public String setStyle(String language){
      
       if(locale.getLanguage().equals(language))
           return "lang_enabled";
       else
           return "lang_disabled";
    }//setStyle

}//class
