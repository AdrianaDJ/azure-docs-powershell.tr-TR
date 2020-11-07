---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 91c23a32fd25c184e46249424b439375caed6ac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759051"
---
# <span data-ttu-id="ffdd8-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="ffdd8-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="ffdd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffdd8-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdd8-103">Veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="ffdd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffdd8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffdd8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffdd8-105">DESCRIPTION</span></span>
<span data-ttu-id="ffdd8-106">**Get-AzSqlDatabaseActivity** cmdlet 'ı Azure SQL veritabanındaki veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="ffdd8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffdd8-107">EXAMPLES</span></span>

### <span data-ttu-id="ffdd8-108">Örnek 1: tüm SQL veritabanı örneklerinin durumunu al</span><span class="sxs-lookup"><span data-stu-id="ffdd8-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ffdd8-109">Bu komut, ElasticPool01 adındaki bir esnek havuzda tüm SQL veritabanı örneklerinin işlem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="ffdd8-110">Örnek 2: tüm SQL veritabanı işlemleri için durum alma</span><span class="sxs-lookup"><span data-stu-id="ffdd8-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ffdd8-111">Bu komut veritabanındaki tüm SQL veritabanı işlemlerinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="ffdd8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffdd8-112">PARAMETERS</span></span>

### <span data-ttu-id="ffdd8-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ffdd8-113">-DatabaseName</span></span>
<span data-ttu-id="ffdd8-114">Bu cmdlet 'in durumu aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdd8-115">-DefaultProfile</span></span>
<span data-ttu-id="ffdd8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffdd8-117">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="ffdd8-117">-ElasticPoolName</span></span>
<span data-ttu-id="ffdd8-118">Bu cmdlet 'in durumu aldığı elastik veritabanı havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="ffdd8-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ffdd8-119">-OperationId</span></span>
<span data-ttu-id="ffdd8-120">Bu cmdlet 'in aldığı işlemin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffdd8-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffdd8-122">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ffdd8-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ffdd8-123">-ServerName</span></span>
<span data-ttu-id="ffdd8-124">Veritabanını barındıran Microsoft SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="ffdd8-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffdd8-125">-Confirm</span></span>
<span data-ttu-id="ffdd8-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffdd8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffdd8-127">-WhatIf</span></span>
<span data-ttu-id="ffdd8-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffdd8-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffdd8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdd8-130">CommonParameters</span></span>
<span data-ttu-id="ffdd8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdd8-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ffdd8-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdd8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffdd8-133">INPUTS</span></span>

### <span data-ttu-id="ffdd8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ffdd8-134">System.String</span></span>

### <span data-ttu-id="ffdd8-135">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ffdd8-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ffdd8-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffdd8-136">OUTPUTS</span></span>

### <span data-ttu-id="ffdd8-137">Microsoft. Azure. Commands. Sql. Database. model. azures, Databaseactivitymodel</span><span class="sxs-lookup"><span data-stu-id="ffdd8-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="ffdd8-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffdd8-138">NOTES</span></span>

## <span data-ttu-id="ffdd8-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffdd8-139">RELATED LINKS</span></span>
