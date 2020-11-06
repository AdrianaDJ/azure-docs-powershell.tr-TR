---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a37bf2dd4e69352ff33a1f8c886750fec67e52f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591885"
---
# <span data-ttu-id="c6b7c-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c6b7c-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="c6b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b7c-103">Veritabanının denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6b7c-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6b7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b7c-106">**Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet 'i, BIR Azure SQL veritabanının denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="c6b7c-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="c6b7c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6b7c-108">EXAMPLES</span></span>

### <span data-ttu-id="c6b7c-109">Örnek 1: bir Azure SQL veritabanının denetim ilkesini, üzerinde tablo denetimi tanımlanmış olarak alma</span><span class="sxs-lookup"><span data-stu-id="c6b7c-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="c6b7c-110">Örnek 2: blob denetimi tanımlanmış bir Azure SQL veritabanının denetim ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="c6b7c-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="c6b7c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6b7c-111">PARAMETERS</span></span>

### <span data-ttu-id="c6b7c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6b7c-112">-DatabaseName</span></span>
<span data-ttu-id="c6b7c-113">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-113">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c6b7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b7c-114">-DefaultProfile</span></span>
<span data-ttu-id="c6b7c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c6b7c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6b7c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b7c-116">-ResourceGroupName</span></span>
<span data-ttu-id="c6b7c-117">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c6b7c-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6b7c-118">-ServerName</span></span>
<span data-ttu-id="c6b7c-119">Veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-119">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="c6b7c-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6b7c-120">-Confirm</span></span>
<span data-ttu-id="c6b7c-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b7c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b7c-122">-WhatIf</span></span>
<span data-ttu-id="c6b7c-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b7c-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b7c-125">CommonParameters</span></span>
<span data-ttu-id="c6b7c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6b7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b7c-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b7c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b7c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6b7c-128">INPUTS</span></span>

### <span data-ttu-id="c6b7c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c6b7c-129">System.String</span></span>

## <span data-ttu-id="c6b7c-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6b7c-130">OUTPUTS</span></span>

### <span data-ttu-id="c6b7c-131">Microsoft. Azure. Commands. Sql. Auditing. model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c6b7c-131">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="c6b7c-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6b7c-132">NOTES</span></span>

## <span data-ttu-id="c6b7c-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6b7c-133">RELATED LINKS</span></span>

[<span data-ttu-id="c6b7c-134">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="c6b7c-134">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="c6b7c-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c6b7c-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



