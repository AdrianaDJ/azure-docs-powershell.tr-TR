---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108683"
---
# <span data-ttu-id="99811-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="99811-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="99811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99811-102">SYNOPSIS</span></span>
<span data-ttu-id="99811-103">Esnek havuzdaki işlemlerin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="99811-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="99811-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99811-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99811-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99811-105">DESCRIPTION</span></span>
<span data-ttu-id="99811-106">**Get-AzSqlElasticPoolActivity** cmdlet 'ı BIR Azure SQL veritabanı için esnek havuzda işlemlerin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="99811-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="99811-107">Havuz oluşturma ve yapılandırma güncelleştirmelerinin durumunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99811-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="99811-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99811-108">EXAMPLES</span></span>

### <span data-ttu-id="99811-109">Örnek 1: esnek bir havuzun işlemlerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="99811-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="99811-110">Bu komut, ElasticPool01 adlı esnek havuz işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="99811-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="99811-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99811-111">PARAMETERS</span></span>

### <span data-ttu-id="99811-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99811-112">-DefaultProfile</span></span>
<span data-ttu-id="99811-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="99811-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99811-114">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="99811-114">-ElasticPoolName</span></span>
<span data-ttu-id="99811-115">Esnek bir havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99811-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="99811-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="99811-116">-OperationId</span></span>
<span data-ttu-id="99811-117">Alınacak işlemin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="99811-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="99811-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99811-118">-ResourceGroupName</span></span>
<span data-ttu-id="99811-119">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99811-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="99811-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99811-120">-ServerName</span></span>
<span data-ttu-id="99811-121">Elastik havuz içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99811-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="99811-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="99811-122">-Confirm</span></span>
<span data-ttu-id="99811-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99811-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99811-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99811-124">-WhatIf</span></span>
<span data-ttu-id="99811-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99811-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99811-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99811-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99811-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99811-127">CommonParameters</span></span>
<span data-ttu-id="99811-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99811-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99811-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99811-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99811-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99811-130">INPUTS</span></span>

### <span data-ttu-id="99811-131">System. String</span><span class="sxs-lookup"><span data-stu-id="99811-131">System.String</span></span>

### <span data-ttu-id="99811-132">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="99811-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="99811-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99811-133">OUTPUTS</span></span>

### <span data-ttu-id="99811-134">Microsoft. Azure. Commands. Sql. Elaçıkartma. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="99811-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="99811-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99811-135">NOTES</span></span>

## <span data-ttu-id="99811-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99811-136">RELATED LINKS</span></span>

[<span data-ttu-id="99811-137">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99811-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="99811-138">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="99811-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="99811-139">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99811-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="99811-140">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99811-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="99811-141">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99811-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


