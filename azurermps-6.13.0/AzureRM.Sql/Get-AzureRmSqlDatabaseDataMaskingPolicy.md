---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 6b787e3347c20e011193d0b3968e036d53f62226
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591884"
---
# <span data-ttu-id="d53eb-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="d53eb-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="d53eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d53eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d53eb-103">Veritabanı için veri maskeleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d53eb-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d53eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d53eb-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d53eb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d53eb-105">DESCRIPTION</span></span>
<span data-ttu-id="d53eb-106">**Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet 'i, BIR Azure SQL veritabanının veri maskeleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d53eb-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="d53eb-107">Bu cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d53eb-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d53eb-108">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d53eb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d53eb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d53eb-109">EXAMPLES</span></span>

### <span data-ttu-id="d53eb-110">Örnek 1: Azure SQL veritabanı için veri maskeleme ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="d53eb-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="d53eb-111">Bu komut, sunucu server01 ResourceGroup01 kaynak grubundaki veri maskeleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d53eb-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="d53eb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d53eb-112">PARAMETERS</span></span>

### <span data-ttu-id="d53eb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d53eb-113">-DatabaseName</span></span>
<span data-ttu-id="d53eb-114">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d53eb-114">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d53eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53eb-115">-DefaultProfile</span></span>
<span data-ttu-id="d53eb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d53eb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d53eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d53eb-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d53eb-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d53eb-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d53eb-119">-ServerName</span></span>
<span data-ttu-id="d53eb-120">Veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d53eb-120">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d53eb-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d53eb-121">-Confirm</span></span>
<span data-ttu-id="d53eb-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d53eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d53eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53eb-123">-WhatIf</span></span>
<span data-ttu-id="d53eb-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d53eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53eb-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d53eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d53eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53eb-126">CommonParameters</span></span>
<span data-ttu-id="d53eb-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d53eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53eb-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53eb-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d53eb-129">INPUTS</span></span>

### <span data-ttu-id="d53eb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d53eb-130">System.String</span></span>

## <span data-ttu-id="d53eb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d53eb-131">OUTPUTS</span></span>

### <span data-ttu-id="d53eb-132">Microsoft. Azure. Commands. Sql. Datamaskeleme. model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d53eb-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="d53eb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d53eb-133">NOTES</span></span>

## <span data-ttu-id="d53eb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d53eb-134">RELATED LINKS</span></span>

[<span data-ttu-id="d53eb-135">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d53eb-135">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d53eb-136">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d53eb-136">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d53eb-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d53eb-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d53eb-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="d53eb-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="d53eb-139">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d53eb-139">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


