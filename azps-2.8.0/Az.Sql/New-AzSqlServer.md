---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933566"
---
# <span data-ttu-id="1fb06-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fb06-101">New-AzSqlServer</span></span>

## <span data-ttu-id="1fb06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb06-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb06-103">SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fb06-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="1fb06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fb06-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fb06-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb06-106">**New-AzSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fb06-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="1fb06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fb06-107">EXAMPLES</span></span>

### <span data-ttu-id="1fb06-108">Örnek 1: yeni Azure SQL veritabanı sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="1fb06-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="1fb06-109">Bu komut 12 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fb06-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="1fb06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fb06-110">PARAMETERS</span></span>

### <span data-ttu-id="1fb06-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1fb06-111">-AsJob</span></span>
<span data-ttu-id="1fb06-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1fb06-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fb06-113">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="1fb06-113">-AssignIdentity</span></span>
<span data-ttu-id="1fb06-114">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="1fb06-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1fb06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb06-115">-DefaultProfile</span></span>
<span data-ttu-id="1fb06-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1fb06-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fb06-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="1fb06-117">-Location</span></span>
<span data-ttu-id="1fb06-118">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb06-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="1fb06-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb06-119">-ResourceGroupName</span></span>
<span data-ttu-id="1fb06-120">Bu cmdlet 'in sunucuya atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb06-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="1fb06-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fb06-121">-ServerName</span></span>
<span data-ttu-id="1fb06-122">Yeni sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb06-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="1fb06-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="1fb06-123">-ServerVersion</span></span>
<span data-ttu-id="1fb06-124">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb06-124">Specifies the version of the new server.</span></span> <span data-ttu-id="1fb06-125">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="1fb06-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="1fb06-126">Sürüm 11 sunucusu oluşturmak için 2,0 veya sürüm 12 sunucusu oluşturmak için 12,0.</span><span class="sxs-lookup"><span data-stu-id="1fb06-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="1fb06-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="1fb06-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="1fb06-128">Yeni sunucunun SQL veritabanı sunucusu yöneticisi kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb06-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="1fb06-129">**PSCredential** nesnesi almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1fb06-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="1fb06-130">Daha fazla bilgi için yazın `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1fb06-130">For more information, type `Get-Help
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

### <span data-ttu-id="1fb06-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="1fb06-131">-Tags</span></span>
<span data-ttu-id="1fb06-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1fb06-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1fb06-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1fb06-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1fb06-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1fb06-134">-Confirm</span></span>
<span data-ttu-id="1fb06-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1fb06-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb06-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb06-136">-WhatIf</span></span>
<span data-ttu-id="1fb06-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1fb06-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fb06-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1fb06-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb06-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb06-139">CommonParameters</span></span>
<span data-ttu-id="1fb06-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fb06-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb06-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1fb06-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb06-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fb06-142">INPUTS</span></span>

### <span data-ttu-id="1fb06-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb06-143">System.String</span></span>

## <span data-ttu-id="1fb06-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fb06-144">OUTPUTS</span></span>

### <span data-ttu-id="1fb06-145">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="1fb06-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1fb06-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fb06-146">NOTES</span></span>

## <span data-ttu-id="1fb06-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fb06-147">RELATED LINKS</span></span>

[<span data-ttu-id="1fb06-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fb06-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="1fb06-149">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fb06-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="1fb06-150">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1fb06-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="1fb06-151">Yeni-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1fb06-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="1fb06-152">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1fb06-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
