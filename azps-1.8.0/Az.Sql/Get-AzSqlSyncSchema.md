---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7e6e060b2ad9e05a0a2789202e74f093f0366749
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758912"
---
# <span data-ttu-id="a02b9-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="a02b9-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="a02b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a02b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a02b9-103">Bir üye veritabanının veya hub veritabanının eşitleme şemasıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a02b9-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="a02b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a02b9-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a02b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a02b9-105">DESCRIPTION</span></span>
<span data-ttu-id="a02b9-106">**Get-AzSqlSyncSchema** cmdlet 'i, bir üye veritabanının veya hub veritabanının eşitleme şemasıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="a02b9-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="a02b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a02b9-107">EXAMPLES</span></span>

### <span data-ttu-id="a02b9-108">Örnek 1,1: hub veritabanı için eşitleme şemasını alma</span><span class="sxs-lookup"><span data-stu-id="a02b9-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="a02b9-109">Bu komut, syncGroup01 eşitleme grubundaki hub veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="a02b9-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="a02b9-110">Örnek 1,2: hub veritabanı için eşitleme şemasını alma ve tabloları genişletme</span><span class="sxs-lookup"><span data-stu-id="a02b9-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="a02b9-111">Bu komut, syncGroup01 ve tabloları Genişlet özelliğindeki hub veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="a02b9-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="a02b9-112">Örnek 2: bir üye veritabanı için eşitleme şemasını alma</span><span class="sxs-lookup"><span data-stu-id="a02b9-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="a02b9-113">Bu komut, syncMember01 eşitleme üyesinde üye veritabanı için eşitleme şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="a02b9-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="a02b9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a02b9-114">PARAMETERS</span></span>

### <span data-ttu-id="a02b9-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a02b9-115">-DatabaseName</span></span>
<span data-ttu-id="a02b9-116">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="a02b9-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a02b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02b9-117">-DefaultProfile</span></span>
<span data-ttu-id="a02b9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a02b9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a02b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="a02b9-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a02b9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a02b9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a02b9-121">-ServerName</span></span>
<span data-ttu-id="a02b9-122">Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="a02b9-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a02b9-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a02b9-123">-SyncGroupName</span></span>
<span data-ttu-id="a02b9-124">Eşitleme grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a02b9-124">The sync group name.</span></span>

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

### <span data-ttu-id="a02b9-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="a02b9-125">-SyncMemberName</span></span>
<span data-ttu-id="a02b9-126">Eşitleme üye adı.</span><span class="sxs-lookup"><span data-stu-id="a02b9-126">The sync member name.</span></span>

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

### <span data-ttu-id="a02b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02b9-127">CommonParameters</span></span>
<span data-ttu-id="a02b9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a02b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02b9-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a02b9-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02b9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a02b9-130">INPUTS</span></span>

### <span data-ttu-id="a02b9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a02b9-131">System.String</span></span>

## <span data-ttu-id="a02b9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a02b9-132">OUTPUTS</span></span>

### <span data-ttu-id="a02b9-133">Microsoft. Azure. Commands. Sql. DataSync. model. Azurestabsyncfullschemamodel</span><span class="sxs-lookup"><span data-stu-id="a02b9-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="a02b9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a02b9-134">NOTES</span></span>

## <span data-ttu-id="a02b9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a02b9-135">RELATED LINKS</span></span>