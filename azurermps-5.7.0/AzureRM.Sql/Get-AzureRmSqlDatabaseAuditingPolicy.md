---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 4d15400da4105f719f5948a53512f6c33cbd3bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763538"
---
# <span data-ttu-id="ee5c2-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="ee5c2-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="ee5c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5c2-103">Veritabanının denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee5c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee5c2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee5c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee5c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5c2-106">**Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet 'i, BIR Azure SQL veritabanının denetim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="ee5c2-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="ee5c2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee5c2-108">EXAMPLES</span></span>

### <span data-ttu-id="ee5c2-109">Örnek 1: bir Azure SQL veritabanının denetim ilkesini, üzerinde tablo denetimi tanımlanmış olarak alma</span><span class="sxs-lookup"><span data-stu-id="ee5c2-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
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

### <span data-ttu-id="ee5c2-110">Örnek 2: blob denetimi tanımlanmış bir Azure SQL veritabanının denetim ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="ee5c2-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="ee5c2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee5c2-111">PARAMETERS</span></span>

### <span data-ttu-id="ee5c2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee5c2-112">-DatabaseName</span></span>
<span data-ttu-id="ee5c2-113">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-113">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5c2-114">-DefaultProfile</span></span>
<span data-ttu-id="ee5c2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee5c2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee5c2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5c2-116">-ResourceGroupName</span></span>
<span data-ttu-id="ee5c2-117">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-117">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5c2-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee5c2-118">-ServerName</span></span>
<span data-ttu-id="ee5c2-119">Veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-119">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5c2-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee5c2-120">-Confirm</span></span>
<span data-ttu-id="ee5c2-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5c2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5c2-122">-WhatIf</span></span>
<span data-ttu-id="ee5c2-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5c2-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5c2-125">CommonParameters</span></span>
<span data-ttu-id="ee5c2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5c2-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5c2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5c2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee5c2-128">INPUTS</span></span>

### <span data-ttu-id="ee5c2-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ee5c2-129">None</span></span>
<span data-ttu-id="ee5c2-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ee5c2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee5c2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee5c2-131">OUTPUTS</span></span>

### <span data-ttu-id="ee5c2-132">Microsoft. Azure. Commands. Sql. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ee5c2-132">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="ee5c2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee5c2-133">NOTES</span></span>

## <span data-ttu-id="ee5c2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee5c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="ee5c2-135">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ee5c2-135">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="ee5c2-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="ee5c2-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



