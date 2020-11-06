---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: a6b5b21b8911aa8d156ced40476d1b0ecadad361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588730"
---
# <span data-ttu-id="a09b3-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a09b3-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="a09b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a09b3-102">SYNOPSIS</span></span>
<span data-ttu-id="a09b3-103">Elastik bir veritabanı havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="a09b3-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a09b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a09b3-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a09b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a09b3-105">DESCRIPTION</span></span>
<span data-ttu-id="a09b3-106">**Remove-Azurermsqlelak,** BIR Azure SQL veritabanı esnek havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="a09b3-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="a09b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a09b3-107">EXAMPLES</span></span>

### <span data-ttu-id="a09b3-108">Örnek 1: esnek havuz silme</span><span class="sxs-lookup"><span data-stu-id="a09b3-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a09b3-109">Bu komut, ElasticPool01 adlı bir esnek havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="a09b3-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="a09b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a09b3-110">PARAMETERS</span></span>

### <span data-ttu-id="a09b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09b3-111">-DefaultProfile</span></span>
<span data-ttu-id="a09b3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a09b3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a09b3-113">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="a09b3-113">-ElasticPoolName</span></span>
<span data-ttu-id="a09b3-114">Bu cmdlet 'in sildiği esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a09b3-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09b3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a09b3-115">-Force</span></span>
<span data-ttu-id="a09b3-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a09b3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="a09b3-118">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a09b3-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="a09b3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a09b3-119">-ServerName</span></span>
<span data-ttu-id="a09b3-120">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a09b3-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="a09b3-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a09b3-121">-Confirm</span></span>
<span data-ttu-id="a09b3-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a09b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09b3-123">-WhatIf</span></span>
<span data-ttu-id="a09b3-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a09b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09b3-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a09b3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09b3-126">CommonParameters</span></span>
<span data-ttu-id="a09b3-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a09b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09b3-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09b3-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a09b3-129">INPUTS</span></span>

### <span data-ttu-id="a09b3-130">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="a09b3-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a09b3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a09b3-131">OUTPUTS</span></span>

### <span data-ttu-id="a09b3-132">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="a09b3-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a09b3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a09b3-133">NOTES</span></span>

## <span data-ttu-id="a09b3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a09b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="a09b3-135">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a09b3-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a09b3-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a09b3-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="a09b3-137">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="a09b3-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="a09b3-138">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a09b3-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a09b3-139">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a09b3-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a09b3-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a09b3-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


