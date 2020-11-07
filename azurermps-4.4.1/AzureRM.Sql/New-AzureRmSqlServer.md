---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763094"
---
# <span data-ttu-id="639d1-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="639d1-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="639d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="639d1-102">SYNOPSIS</span></span>
<span data-ttu-id="639d1-103">SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="639d1-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="639d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="639d1-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="639d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="639d1-105">DESCRIPTION</span></span>
<span data-ttu-id="639d1-106">**New-AzureRmSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="639d1-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="639d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="639d1-107">EXAMPLES</span></span>

### <span data-ttu-id="639d1-108">Örnek 1: yeni Azure SQL veritabanı sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="639d1-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="639d1-109">Bu komut 12 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="639d1-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="639d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="639d1-110">PARAMETERS</span></span>

### <span data-ttu-id="639d1-111">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="639d1-111">-AssignIdentity</span></span>
<span data-ttu-id="639d1-112">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="639d1-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="639d1-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="639d1-113">-Location</span></span>
<span data-ttu-id="639d1-114">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="639d1-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="639d1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639d1-115">-ResourceGroupName</span></span>
<span data-ttu-id="639d1-116">Bu cmdlet 'in sunucuya atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="639d1-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="639d1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="639d1-117">-ServerName</span></span>
<span data-ttu-id="639d1-118">Yeni sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="639d1-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="639d1-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="639d1-119">-ServerVersion</span></span>
<span data-ttu-id="639d1-120">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="639d1-120">Specifies the version of the new server.</span></span> <span data-ttu-id="639d1-121">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="639d1-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="639d1-122">Sürüm 11 sunucusu oluşturmak için 2,0 veya sürüm 12 sunucusu oluşturmak için 12,0.</span><span class="sxs-lookup"><span data-stu-id="639d1-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="639d1-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="639d1-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="639d1-124">Yeni sunucunun SQL veritabanı sunucusu yöneticisi kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="639d1-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="639d1-125">**PSCredential** nesnesi almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="639d1-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="639d1-126">Daha fazla bilgi için yazın `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="639d1-126">For more information, type `Get-Help
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

### <span data-ttu-id="639d1-127">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="639d1-127">-Tags</span></span>
<span data-ttu-id="639d1-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="639d1-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="639d1-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="639d1-129">For example:</span></span>

<span data-ttu-id="639d1-130">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="639d1-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="639d1-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="639d1-131">-Confirm</span></span>
<span data-ttu-id="639d1-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="639d1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="639d1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="639d1-133">-WhatIf</span></span>
<span data-ttu-id="639d1-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="639d1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="639d1-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="639d1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="639d1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639d1-136">-DefaultProfile</span></span>
<span data-ttu-id="639d1-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="639d1-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="639d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639d1-138">CommonParameters</span></span>
<span data-ttu-id="639d1-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="639d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639d1-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="639d1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639d1-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="639d1-141">INPUTS</span></span>

## <span data-ttu-id="639d1-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="639d1-142">OUTPUTS</span></span>

### <span data-ttu-id="639d1-143">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="639d1-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="639d1-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="639d1-144">NOTES</span></span>

## <span data-ttu-id="639d1-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="639d1-145">RELATED LINKS</span></span>

[<span data-ttu-id="639d1-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="639d1-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="639d1-147">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="639d1-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="639d1-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="639d1-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="639d1-149">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="639d1-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="639d1-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="639d1-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
