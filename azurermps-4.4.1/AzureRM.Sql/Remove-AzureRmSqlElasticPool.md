---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591767"
---
# <span data-ttu-id="6306f-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6306f-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="6306f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6306f-102">SYNOPSIS</span></span>
<span data-ttu-id="6306f-103">Elastik bir veritabanı havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="6306f-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6306f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6306f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6306f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6306f-105">DESCRIPTION</span></span>
<span data-ttu-id="6306f-106">**Remove-Azurermsqlelak,** BIR Azure SQL veritabanı esnek havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="6306f-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="6306f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6306f-107">EXAMPLES</span></span>

### <span data-ttu-id="6306f-108">Örnek 1: esnek havuz silme</span><span class="sxs-lookup"><span data-stu-id="6306f-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6306f-109">Bu komut, ElasticPool01 adlı bir esnek havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="6306f-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="6306f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6306f-110">PARAMETERS</span></span>

### <span data-ttu-id="6306f-111">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="6306f-111">-ElasticPoolName</span></span>
<span data-ttu-id="6306f-112">Bu cmdlet 'in sildiği esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6306f-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6306f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6306f-113">-Force</span></span>
<span data-ttu-id="6306f-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6306f-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6306f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6306f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6306f-116">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6306f-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="6306f-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6306f-117">-ServerName</span></span>
<span data-ttu-id="6306f-118">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6306f-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6306f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6306f-119">-Confirm</span></span>
<span data-ttu-id="6306f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6306f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6306f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6306f-121">-WhatIf</span></span>
<span data-ttu-id="6306f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6306f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6306f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6306f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6306f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6306f-124">-DefaultProfile</span></span>
<span data-ttu-id="6306f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6306f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6306f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6306f-126">CommonParameters</span></span>
<span data-ttu-id="6306f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6306f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6306f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6306f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6306f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6306f-129">INPUTS</span></span>

### <span data-ttu-id="6306f-130">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="6306f-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6306f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6306f-131">OUTPUTS</span></span>

### <span data-ttu-id="6306f-132">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="6306f-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6306f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6306f-133">NOTES</span></span>

## <span data-ttu-id="6306f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6306f-134">RELATED LINKS</span></span>

[<span data-ttu-id="6306f-135">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="6306f-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="6306f-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6306f-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="6306f-137">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="6306f-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="6306f-138">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="6306f-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="6306f-139">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="6306f-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="6306f-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="6306f-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


