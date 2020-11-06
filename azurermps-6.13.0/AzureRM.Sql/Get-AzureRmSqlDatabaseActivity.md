---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 08c5778002a80bb4fb2effdd977f134079f3aa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591894"
---
# <span data-ttu-id="28b1f-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="28b1f-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="28b1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="28b1f-103">Veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="28b1f-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28b1f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="28b1f-106">**Get-AzureRmSqlDatabaseActivity** cmdlet 'ı Azure SQL veritabanındaki veritabanı işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="28b1f-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="28b1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="28b1f-108">Örnek 1: tüm SQL veritabanı örneklerinin durumunu al</span><span class="sxs-lookup"><span data-stu-id="28b1f-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="28b1f-109">Bu komut, ElasticPool01 adındaki bir esnek havuzda tüm SQL veritabanı örneklerinin işlem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="28b1f-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="28b1f-110">Örnek 2: tüm SQL veritabanı işlemleri için durum alma</span><span class="sxs-lookup"><span data-stu-id="28b1f-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="28b1f-111">Bu komut veritabanındaki tüm SQL veritabanı işlemlerinin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="28b1f-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="28b1f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28b1f-112">PARAMETERS</span></span>

### <span data-ttu-id="28b1f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28b1f-113">-DatabaseName</span></span>
<span data-ttu-id="28b1f-114">Bu cmdlet 'in durumu aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28b1f-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="28b1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b1f-115">-DefaultProfile</span></span>
<span data-ttu-id="28b1f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28b1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b1f-117">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="28b1f-117">-ElasticPoolName</span></span>
<span data-ttu-id="28b1f-118">Bu cmdlet 'in durumu aldığı elastik veritabanı havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28b1f-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="28b1f-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="28b1f-119">-OperationId</span></span>
<span data-ttu-id="28b1f-120">Bu cmdlet 'in aldığı işlemin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="28b1f-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="28b1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="28b1f-122">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28b1f-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="28b1f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28b1f-123">-ServerName</span></span>
<span data-ttu-id="28b1f-124">Veritabanını barındıran Microsoft SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="28b1f-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="28b1f-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="28b1f-125">-Confirm</span></span>
<span data-ttu-id="28b1f-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28b1f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b1f-127">-WhatIf</span></span>
<span data-ttu-id="28b1f-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28b1f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b1f-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28b1f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b1f-130">CommonParameters</span></span>
<span data-ttu-id="28b1f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28b1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b1f-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b1f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28b1f-133">INPUTS</span></span>

### <span data-ttu-id="28b1f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="28b1f-134">System.String</span></span>

### <span data-ttu-id="28b1f-135">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="28b1f-135">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="28b1f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28b1f-136">OUTPUTS</span></span>

### <span data-ttu-id="28b1f-137">Microsoft. Azure. Commands. Sql. Database. model. azures, Databaseactivitymodel</span><span class="sxs-lookup"><span data-stu-id="28b1f-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="28b1f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28b1f-138">NOTES</span></span>

## <span data-ttu-id="28b1f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28b1f-139">RELATED LINKS</span></span>
