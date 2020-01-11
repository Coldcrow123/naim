package com.faruky.firstplugin;
import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.entity.Player;
import org.bukkit.plugin.java.JavaPlugin;
import net.md_5.bungee.api.ChatColor;

public class main extends JavaPlugin {
	
	
	    
	    @Override
	    public void onEnable() {
	        System.out.println("TEST PLUGIN ENABLED");
	        

	        
	    }
	    
	    @Override
	    public void onDisable() {
	        System.out.println("TEST PLUGIN DISABLED");
	        
	    }
	    
	    public boolean onCommand(CommandSender sender, Command cmd, String label, String[] args) {
			
	    	if(sender instanceof Player) {
	    	Player player = (Player) sender;

	    	if (cmd.getName().equals("heal")) {	
	    		
	    		player.sendMessage(ChatColor.GRAY + "Hello, " + ChatColor.GREEN + player.getName() + ChatColor.GRAY + " your health been restored");
	    		player.setHealth(20.0);
	    		
	    	}
	    			
	    			
	    	
	    	if (cmd.getName().equals("feed")) {	
				
	    		player.sendMessage(ChatColor.GRAY + "Hello, " + ChatColor.GREEN + player.getName() + ChatColor.GRAY + " your food been restored");
	    		player.setFoodLevel(20);
	    			 
	    			
	    	}
	    	  
	    	
	    } 
	    else 
    		System.out.println("You cannot use this command through console!");

    		
	    	

		    	return false;
	    		
	}
	    	
	    	
	    	
}
	
