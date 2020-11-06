---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: b78bcf228012edd022f9551a5834c61cebc8d278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591890"
---
# <span data-ttu-id="e769b-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="e769b-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="e769b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e769b-102">SYNOPSIS</span></span>
<span data-ttu-id="e769b-103">Bir Azure SQL veritabanının denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e769b-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e769b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e769b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e769b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e769b-105">DESCRIPTION</span></span>
<span data-ttu-id="e769b-106">**Get-AzureRmSqlDatabaseAuditing** cmdlet 'i, BIR Azure SQL veritabanının denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e769b-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="e769b-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e769b-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="e769b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e769b-108">EXAMPLES</span></span>

### <span data-ttu-id="e769b-109">Örnek 1: Azure SQL veritabanının denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="e769b-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

## <span data-ttu-id="e769b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e769b-110">PARAMETERS</span></span>

### <span data-ttu-id="e769b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e769b-111">-DatabaseName</span></span>
<span data-ttu-id="e769b-112">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="e769b-112">SQL Database name.</span></span>

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

### <span data-ttu-id="e769b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e769b-113">-DefaultProfile</span></span>
<span data-ttu-id="e769b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e769b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e769b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e769b-115">-ResourceGroupName</span></span>
<span data-ttu-id="e769b-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e769b-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="e769b-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e769b-117">-ServerName</span></span>
<span data-ttu-id="e769b-118">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="e769b-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="e769b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e769b-119">-Confirm</span></span>
<span data-ttu-id="e769b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e769b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e769b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e769b-121">-WhatIf</span></span>
<span data-ttu-id="e769b-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e769b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e769b-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e769b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e769b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e769b-124">CommonParameters</span></span>
<span data-ttu-id="e769b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e769b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e769b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e769b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e769b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e769b-127">INPUTS</span></span>

## <span data-ttu-id="e769b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e769b-128">OUTPUTS</span></span>

### <span data-ttu-id="e769b-129">Microsoft. Azure. Commands. Sql. Auditing. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="e769b-129">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="e769b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e769b-130">NOTES</span></span>

## <span data-ttu-id="e769b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e769b-131">RELATED LINKS</span></span>
