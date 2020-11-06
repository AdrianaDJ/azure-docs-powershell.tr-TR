---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594163"
---
# <span data-ttu-id="3f1bc-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="3f1bc-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="3f1bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1bc-103">Elastik veritabanlarının taşınması durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f1bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f1bc-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="3f1bc-106">**Get-AzureRmSqlDatabaseActivity** cmdlet 'ı, Azure SQL veritabanında esnek bir veritabanı havuzuna taşınan veya olmayan elastik veritabanlarının durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="3f1bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f1bc-107">EXAMPLES</span></span>

### <span data-ttu-id="3f1bc-108">Örnek 1: tüm SQL veritabanı örneklerinin durumunu al</span><span class="sxs-lookup"><span data-stu-id="3f1bc-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="3f1bc-109">Bu komut, ElasticPool01 adındaki bir esnek havuzda tüm SQL veritabanı örneklerinin işlem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="3f1bc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f1bc-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1bc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f1bc-111">-DatabaseName</span></span>
<span data-ttu-id="3f1bc-112">Bu cmdlet 'in durumu aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3f1bc-113">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="3f1bc-113">-ElasticPoolName</span></span>
<span data-ttu-id="3f1bc-114">Bu cmdlet 'in durumu aldığı elastik veritabanı havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="3f1bc-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3f1bc-115">-OperationId</span></span>
<span data-ttu-id="3f1bc-116">Bu cmdlet 'in aldığı işlemin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3f1bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f1bc-118">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3f1bc-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f1bc-119">-ServerName</span></span>
<span data-ttu-id="3f1bc-120">Elastik veritabanı havuzunu barındıran Microsoft SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="3f1bc-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f1bc-121">-Confirm</span></span>
<span data-ttu-id="3f1bc-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1bc-123">-WhatIf</span></span>
<span data-ttu-id="3f1bc-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1bc-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1bc-126">-DefaultProfile</span></span>
<span data-ttu-id="3f1bc-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f1bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1bc-128">CommonParameters</span></span>
<span data-ttu-id="3f1bc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f1bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1bc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1bc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f1bc-131">INPUTS</span></span>

## <span data-ttu-id="3f1bc-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f1bc-132">OUTPUTS</span></span>

### <span data-ttu-id="3f1bc-133">Microsoft. Azure. Commands. Sql. Database. model. azures, Databaseactivitymodel</span><span class="sxs-lookup"><span data-stu-id="3f1bc-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="3f1bc-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f1bc-134">NOTES</span></span>

## <span data-ttu-id="3f1bc-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f1bc-135">RELATED LINKS</span></span>

