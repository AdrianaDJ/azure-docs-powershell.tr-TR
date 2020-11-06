---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 208d72607397cb61e098052cd1835f44d4e0e4a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590828"
---
# <span data-ttu-id="4358f-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="4358f-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="4358f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4358f-102">SYNOPSIS</span></span>
<span data-ttu-id="4358f-103">SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4358f-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4358f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4358f-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4358f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4358f-105">DESCRIPTION</span></span>
<span data-ttu-id="4358f-106">**New-AzureRmSqlServer** cmdlet 'ı BIR Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4358f-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="4358f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4358f-107">EXAMPLES</span></span>

### <span data-ttu-id="4358f-108">Örnek 1: yeni Azure SQL veritabanı sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="4358f-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="4358f-109">Bu komut 12 Azure SQL veritabanı sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4358f-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="4358f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4358f-110">PARAMETERS</span></span>

### <span data-ttu-id="4358f-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4358f-111">-AsJob</span></span>
<span data-ttu-id="4358f-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4358f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4358f-113">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="4358f-113">-AssignIdentity</span></span>
<span data-ttu-id="4358f-114">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="4358f-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4358f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4358f-115">-DefaultProfile</span></span>
<span data-ttu-id="4358f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4358f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4358f-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="4358f-117">-Location</span></span>
<span data-ttu-id="4358f-118">Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4358f-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="4358f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4358f-119">-ResourceGroupName</span></span>
<span data-ttu-id="4358f-120">Bu cmdlet 'in sunucuya atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4358f-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="4358f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4358f-121">-ServerName</span></span>
<span data-ttu-id="4358f-122">Yeni sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4358f-122">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="4358f-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="4358f-123">-ServerVersion</span></span>
<span data-ttu-id="4358f-124">Yeni sunucunun sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4358f-124">Specifies the version of the new server.</span></span> <span data-ttu-id="4358f-125">Bu parametre için kabul edilebilir değerler: 2,0 ve 12,0.</span><span class="sxs-lookup"><span data-stu-id="4358f-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="4358f-126">Sürüm 11 sunucusu oluşturmak için 2,0 veya sürüm 12 sunucusu oluşturmak için 12,0.</span><span class="sxs-lookup"><span data-stu-id="4358f-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="4358f-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="4358f-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="4358f-128">Yeni sunucunun SQL veritabanı sunucusu yöneticisi kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4358f-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="4358f-129">**PSCredential** nesnesi almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4358f-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="4358f-130">Daha fazla bilgi için yazın `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4358f-130">For more information, type `Get-Help
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

### <span data-ttu-id="4358f-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="4358f-131">-Tags</span></span>
<span data-ttu-id="4358f-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4358f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4358f-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4358f-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4358f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4358f-134">-Confirm</span></span>
<span data-ttu-id="4358f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4358f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4358f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4358f-136">-WhatIf</span></span>
<span data-ttu-id="4358f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4358f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4358f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4358f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4358f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4358f-139">CommonParameters</span></span>
<span data-ttu-id="4358f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4358f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4358f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4358f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4358f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4358f-142">INPUTS</span></span>

### <span data-ttu-id="4358f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4358f-143">System.String</span></span>

## <span data-ttu-id="4358f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4358f-144">OUTPUTS</span></span>

### <span data-ttu-id="4358f-145">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="4358f-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="4358f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4358f-146">NOTES</span></span>

## <span data-ttu-id="4358f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4358f-147">RELATED LINKS</span></span>

[<span data-ttu-id="4358f-148">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="4358f-148">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="4358f-149">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="4358f-149">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="4358f-150">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="4358f-150">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="4358f-151">Yeni-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4358f-151">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="4358f-152">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="4358f-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
