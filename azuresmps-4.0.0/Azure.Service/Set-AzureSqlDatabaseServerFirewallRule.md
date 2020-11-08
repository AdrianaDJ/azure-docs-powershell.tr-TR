---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105863"
---
# <span data-ttu-id="7a960-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a960-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="7a960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a960-102">SYNOPSIS</span></span>
<span data-ttu-id="7a960-103">Azure SQL veritabanı sunucusunda varolan bir güvenlik duvarı kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7a960-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="7a960-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a960-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a960-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a960-105">DESCRIPTION</span></span>
<span data-ttu-id="7a960-106">**Set-azures, Databaseserverfirewallrule** cmdlet 'i, BELIRTILEN Azure SQL veritabanı sunucusu örneğindeki varolan güvenlik DUVARıNıN başlangıç IP adresini ve bitiş IP adresi değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7a960-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="7a960-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a960-107">EXAMPLES</span></span>

### <span data-ttu-id="7a960-108">Örnek 1: güvenlik duvarı kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="7a960-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="7a960-109">Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusunda FirewallRule24 adındaki güvenlik duvarı kuralının başlangıç IP adresini ve bitiş IP adresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7a960-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="7a960-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a960-110">PARAMETERS</span></span>

### <span data-ttu-id="7a960-111">-Endıadaddress</span><span class="sxs-lookup"><span data-stu-id="7a960-111">-EndIpAddress</span></span>
<span data-ttu-id="7a960-112">Bu kuralın IP adresi aralığının bitiş değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a960-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7a960-113">-Force</span></span>
<span data-ttu-id="7a960-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7a960-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="7a960-115">-Profile</span></span>
<span data-ttu-id="7a960-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a960-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a960-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7a960-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7a960-118">-RuleName</span></span>
<span data-ttu-id="7a960-119">Bu cmdlet 'in değiştirdiği güvenlik duvarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a960-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a960-120">-ServerName</span></span>
<span data-ttu-id="7a960-121">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a960-121">Specifies the name of a server.</span></span>
<span data-ttu-id="7a960-122">Bu cmdlet, bu cmdlet 'in belirttiği sunucuda bir güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7a960-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="7a960-123">Tam DNS adını değil, sunucu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a960-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-124">-Startıpaddress</span><span class="sxs-lookup"><span data-stu-id="7a960-124">-StartIpAddress</span></span>
<span data-ttu-id="7a960-125">Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a960-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a960-126">-Confirm</span></span>
<span data-ttu-id="7a960-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a960-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a960-128">-WhatIf</span></span>
<span data-ttu-id="7a960-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a960-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a960-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a960-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a960-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a960-131">CommonParameters</span></span>
<span data-ttu-id="7a960-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a960-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a960-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a960-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a960-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a960-134">INPUTS</span></span>

### <span data-ttu-id="7a960-135">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="7a960-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="7a960-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a960-136">OUTPUTS</span></span>

### <span data-ttu-id="7a960-137">Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="7a960-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="7a960-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a960-138">NOTES</span></span>

## <span data-ttu-id="7a960-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a960-139">RELATED LINKS</span></span>

[<span data-ttu-id="7a960-140">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="7a960-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="7a960-141">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="7a960-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="7a960-142">Güvenlik duvarı kuralı ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a960-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="7a960-143">Get-Azuressqldatabaseserverfirewallrule</span><span class="sxs-lookup"><span data-stu-id="7a960-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="7a960-144">New-Azuressqldatabaseserverfirewallrule</span><span class="sxs-lookup"><span data-stu-id="7a960-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="7a960-145">Remove-Azuressqldatabaseserverfirewallrule</span><span class="sxs-lookup"><span data-stu-id="7a960-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


