---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 7a28e29e6ee517d15c6edcd462c274ef3a7dbced
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938424"
---
# <span data-ttu-id="0a396-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0a396-101">New-AzSqlServer</span></span>

## <span data-ttu-id="0a396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a396-102">SYNOPSIS</span></span>
<span data-ttu-id="0a396-103">SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a396-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="0a396-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a396-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-PublicNetworkAccess <String>] [-MinimalTlsVersion <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a396-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a396-105">DESCRIPTION</span></span>
<span data-ttu-id="0a396-106">**New-AzSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a396-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="0a396-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a396-107">EXAMPLES</span></span>

### <span data-ttu-id="0a396-108">Örnek 1: yeni Azure SQL veritabanı sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a396-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="0a396-109">Bu komut 12 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0a396-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="0a396-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a396-110">PARAMETERS</span></span>

### <span data-ttu-id="0a396-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="0a396-111">-AsJob</span></span>
<span data-ttu-id="0a396-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0a396-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a396-113">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="0a396-113">-AssignIdentity</span></span>
<span data-ttu-id="0a396-114">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="0a396-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0a396-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a396-115">-DefaultProfile</span></span>
<span data-ttu-id="0a396-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0a396-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a396-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0a396-117">-Location</span></span>
<span data-ttu-id="0a396-118">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a396-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="0a396-119">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0a396-119">-PublicNetworkAccess</span></span>
<span data-ttu-id="0a396-120">Sunucuya genel ağ erişimine izin verilip verilmediğini belirtmek için etkin/devre dışı bayrağı alır.</span><span class="sxs-lookup"><span data-stu-id="0a396-120">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="0a396-121">Devre dışı bırakıldığında, yalnızca özel bağlantılar aracılığıyla yapılan bağlantılar bu sunucuya ulaşabilir.</span><span class="sxs-lookup"><span data-stu-id="0a396-121">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a396-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a396-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a396-123">Bu cmdlet 'in sunucuya atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a396-123">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="0a396-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a396-124">-ServerName</span></span>
<span data-ttu-id="0a396-125">Yeni sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a396-125">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="0a396-126">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="0a396-126">-ServerVersion</span></span>
<span data-ttu-id="0a396-127">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a396-127">Specifies the version of the new server.</span></span> <span data-ttu-id="0a396-128">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="0a396-128">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="0a396-129">Sürüm 11 sunucusu oluşturmak için 2,0 veya sürüm 12 sunucusu oluşturmak için 12,0.</span><span class="sxs-lookup"><span data-stu-id="0a396-129">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="0a396-130">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="0a396-130">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="0a396-131">Yeni sunucunun SQL veritabanı sunucusu yöneticisi kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a396-131">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="0a396-132">**PSCredential** nesnesi almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0a396-132">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="0a396-133">Daha fazla bilgi için yazın `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="0a396-133">For more information, type `Get-Help
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

### <span data-ttu-id="0a396-134">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0a396-134">-MinimalTlsVersion</span></span>
<span data-ttu-id="0a396-135">SQL Server için zorunlu en az TLS sürümü</span><span class="sxs-lookup"><span data-stu-id="0a396-135">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="0a396-136">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="0a396-136">-Tags</span></span>
<span data-ttu-id="0a396-137">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="0a396-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a396-138">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="0a396-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a396-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a396-139">-Confirm</span></span>
<span data-ttu-id="0a396-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a396-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a396-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a396-141">-WhatIf</span></span>
<span data-ttu-id="0a396-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a396-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a396-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a396-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a396-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a396-144">CommonParameters</span></span>
<span data-ttu-id="0a396-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a396-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a396-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a396-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a396-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a396-147">INPUTS</span></span>

### <span data-ttu-id="0a396-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0a396-148">System.String</span></span>

## <span data-ttu-id="0a396-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a396-149">OUTPUTS</span></span>

### <span data-ttu-id="0a396-150">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="0a396-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="0a396-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a396-151">NOTES</span></span>

## <span data-ttu-id="0a396-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a396-152">RELATED LINKS</span></span>

[<span data-ttu-id="0a396-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0a396-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="0a396-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0a396-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="0a396-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0a396-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="0a396-156">Yeni-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0a396-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="0a396-157">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0a396-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
