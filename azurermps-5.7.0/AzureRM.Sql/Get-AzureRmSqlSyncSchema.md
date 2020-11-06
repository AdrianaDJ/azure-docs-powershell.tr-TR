---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 7947b7639678487777c534820656dc0cb3137295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592387"
---
# <span data-ttu-id="7488f-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="7488f-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="7488f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7488f-102">SYNOPSIS</span></span>
<span data-ttu-id="7488f-103">Bir üye veritabanının veya hub veritabanının eşitleme şemasıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7488f-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7488f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7488f-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7488f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7488f-105">DESCRIPTION</span></span>
<span data-ttu-id="7488f-106">**Get-AzureRmSqlSyncSchema** cmdlet 'i, bir üye veritabanının veya hub veritabanının eşitleme şemasıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7488f-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="7488f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7488f-107">EXAMPLES</span></span>

### <span data-ttu-id="7488f-108">Örnek 1,1: hub veritabanı için eşitleme şemasını alma</span><span class="sxs-lookup"><span data-stu-id="7488f-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="7488f-109">Bu komut, syncGroup01 eşitleme grubundaki hub veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="7488f-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="7488f-110">Örnek 1,2: hub veritabanı için eşitleme şemasını alma ve tabloları genişletme</span><span class="sxs-lookup"><span data-stu-id="7488f-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="7488f-111">Bu komut, syncGroup01 ve tabloları Genişlet özelliğindeki hub veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="7488f-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="7488f-112">Örnek 2: bir üye veritabanı için eşitleme şemasını alma</span><span class="sxs-lookup"><span data-stu-id="7488f-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="7488f-113">Bu komut, syncMember01 eşitleme üyesinde üye veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="7488f-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="7488f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7488f-114">PARAMETERS</span></span>

### <span data-ttu-id="7488f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7488f-115">-DatabaseName</span></span>
<span data-ttu-id="7488f-116">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="7488f-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7488f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7488f-117">-DefaultProfile</span></span>
<span data-ttu-id="7488f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7488f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7488f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7488f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7488f-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7488f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7488f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7488f-121">-ServerName</span></span>
<span data-ttu-id="7488f-122">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="7488f-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7488f-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7488f-123">-SyncGroupName</span></span>
<span data-ttu-id="7488f-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7488f-124">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7488f-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="7488f-125">-SyncMemberName</span></span>
<span data-ttu-id="7488f-126">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="7488f-126">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7488f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7488f-127">CommonParameters</span></span>
<span data-ttu-id="7488f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7488f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7488f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7488f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7488f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7488f-130">INPUTS</span></span>

### <span data-ttu-id="7488f-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7488f-131">None</span></span>
<span data-ttu-id="7488f-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7488f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7488f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7488f-133">OUTPUTS</span></span>

### <span data-ttu-id="7488f-134">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncfullschemamodel</span><span class="sxs-lookup"><span data-stu-id="7488f-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="7488f-135">Tablolar: Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncfullschematablemodel</span><span class="sxs-lookup"><span data-stu-id="7488f-135">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="7488f-136">Sütunlar: Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncfullschemacolumnmodel</span><span class="sxs-lookup"><span data-stu-id="7488f-136">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="7488f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7488f-137">NOTES</span></span>

## <span data-ttu-id="7488f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7488f-138">RELATED LINKS</span></span>
