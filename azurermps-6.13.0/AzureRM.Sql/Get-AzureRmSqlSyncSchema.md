---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 38e56102ba544bc56384f0d3ff59bdc8091bdd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593635"
---
# <span data-ttu-id="67b0b-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="67b0b-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="67b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="67b0b-103">Bir üye veritabanının veya hub veritabanının eşitleme şemasıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="67b0b-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67b0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67b0b-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67b0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="67b0b-106">**Get-AzureRmSqlSyncSchema** cmdlet 'i, bir üye veritabanının veya hub veritabanının eşitleme şemasıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="67b0b-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="67b0b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="67b0b-108">Örnek 1,1: hub veritabanı için eşitleme şemasını alma</span><span class="sxs-lookup"><span data-stu-id="67b0b-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="67b0b-109">Bu komut, syncGroup01 eşitleme grubundaki hub veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="67b0b-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="67b0b-110">Örnek 1,2: hub veritabanı için eşitleme şemasını alma ve tabloları genişletme</span><span class="sxs-lookup"><span data-stu-id="67b0b-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
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

<span data-ttu-id="67b0b-111">Bu komut, syncGroup01 ve tabloları Genişlet özelliğindeki hub veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="67b0b-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="67b0b-112">Örnek 2: bir üye veritabanı için eşitleme şemasını alma</span><span class="sxs-lookup"><span data-stu-id="67b0b-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="67b0b-113">Bu komut, syncMember01 eşitleme üyesinde üye veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="67b0b-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="67b0b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67b0b-114">PARAMETERS</span></span>

### <span data-ttu-id="67b0b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67b0b-115">-DatabaseName</span></span>
<span data-ttu-id="67b0b-116">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="67b0b-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="67b0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b0b-117">-DefaultProfile</span></span>
<span data-ttu-id="67b0b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="67b0b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67b0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="67b0b-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="67b0b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="67b0b-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67b0b-121">-ServerName</span></span>
<span data-ttu-id="67b0b-122">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="67b0b-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="67b0b-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="67b0b-123">-SyncGroupName</span></span>
<span data-ttu-id="67b0b-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="67b0b-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b0b-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="67b0b-125">-SyncMemberName</span></span>
<span data-ttu-id="67b0b-126">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="67b0b-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b0b-127">CommonParameters</span></span>
<span data-ttu-id="67b0b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67b0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b0b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b0b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b0b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67b0b-130">INPUTS</span></span>

### <span data-ttu-id="67b0b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="67b0b-131">System.String</span></span>

## <span data-ttu-id="67b0b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67b0b-132">OUTPUTS</span></span>

### <span data-ttu-id="67b0b-133">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncfullschemamodel</span><span class="sxs-lookup"><span data-stu-id="67b0b-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="67b0b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67b0b-134">NOTES</span></span>

## <span data-ttu-id="67b0b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67b0b-135">RELATED LINKS</span></span>
