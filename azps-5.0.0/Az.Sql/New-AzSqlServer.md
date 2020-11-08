---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276668"
---
# <span data-ttu-id="42e45-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="42e45-101">New-AzSqlServer</span></span>

## <span data-ttu-id="42e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e45-102">SYNOPSIS</span></span>
<span data-ttu-id="42e45-103">SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42e45-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="42e45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42e45-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42e45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42e45-105">DESCRIPTION</span></span>
<span data-ttu-id="42e45-106">**New-AzSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42e45-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="42e45-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42e45-107">EXAMPLES</span></span>

### <span data-ttu-id="42e45-108">Örnek 1: yeni Azure SQL veritabanı sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="42e45-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="42e45-109">Bu komut 12 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42e45-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="42e45-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42e45-110">PARAMETERS</span></span>

### <span data-ttu-id="42e45-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="42e45-111">-AsJob</span></span>
<span data-ttu-id="42e45-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="42e45-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-113">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="42e45-113">-AssignIdentity</span></span>
<span data-ttu-id="42e45-114">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="42e45-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e45-115">-DefaultProfile</span></span>
<span data-ttu-id="42e45-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42e45-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="42e45-117">-Location</span></span>
<span data-ttu-id="42e45-118">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="42e45-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="42e45-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="42e45-120">SQL Server için zorunlu en az TLS sürümü</span><span class="sxs-lookup"><span data-stu-id="42e45-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="42e45-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="42e45-122">Sunucuya genel ağ erişimine izin verilip verilmediğini belirtmek için etkin/devre dışı bayrağı alır.</span><span class="sxs-lookup"><span data-stu-id="42e45-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="42e45-123">Devre dışı bırakıldığında, yalnızca özel bağlantılar aracılığıyla yapılan bağlantılar bu sunucuya ulaşabilir.</span><span class="sxs-lookup"><span data-stu-id="42e45-123">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e45-124">-ResourceGroupName</span></span>
<span data-ttu-id="42e45-125">Bu cmdlet 'in sunucuya atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42e45-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42e45-126">-ServerName</span></span>
<span data-ttu-id="42e45-127">Yeni sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42e45-127">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="42e45-128">-ServerVersion</span></span>
<span data-ttu-id="42e45-129">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="42e45-129">Specifies the version of the new server.</span></span> <span data-ttu-id="42e45-130">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="42e45-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="42e45-131">Sürüm 11 sunucusu oluşturmak için 2,0 veya sürüm 12 sunucusu oluşturmak için 12,0.</span><span class="sxs-lookup"><span data-stu-id="42e45-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="42e45-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="42e45-133">Yeni sunucunun SQL veritabanı sunucusu yöneticisi kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="42e45-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="42e45-134">**PSCredential** nesnesi almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="42e45-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="42e45-135">Daha fazla bilgi için yazın `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="42e45-135">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-136">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="42e45-136">-Tags</span></span>
<span data-ttu-id="42e45-137">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="42e45-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42e45-138">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="42e45-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="42e45-139">-Confirm</span></span>
<span data-ttu-id="42e45-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42e45-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e45-141">-WhatIf</span></span>
<span data-ttu-id="42e45-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42e45-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e45-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42e45-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e45-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e45-144">CommonParameters</span></span>
<span data-ttu-id="42e45-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42e45-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e45-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42e45-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e45-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42e45-147">INPUTS</span></span>

### <span data-ttu-id="42e45-148">System. String</span><span class="sxs-lookup"><span data-stu-id="42e45-148">System.String</span></span>

## <span data-ttu-id="42e45-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42e45-149">OUTPUTS</span></span>

### <span data-ttu-id="42e45-150">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="42e45-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="42e45-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42e45-151">NOTES</span></span>

## <span data-ttu-id="42e45-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42e45-152">RELATED LINKS</span></span>

[<span data-ttu-id="42e45-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="42e45-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="42e45-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="42e45-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="42e45-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="42e45-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="42e45-156">Yeni-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="42e45-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="42e45-157">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="42e45-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
