---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: f5e7455a253c86fe363b72c5d4c0e8ff47b96f56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763426"
---
# <span data-ttu-id="69a5e-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="69a5e-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="69a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="69a5e-103">Esnek havuzdaki işlemlerin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="69a5e-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69a5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69a5e-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69a5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="69a5e-106">**Get-AzureRmSqlElasticPoolActivity** cmdlet 'ı BIR Azure SQL veritabanı için esnek havuzda işlemlerin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="69a5e-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="69a5e-107">Havuz oluşturma ve yapılandırma güncelleştirmelerinin durumunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69a5e-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="69a5e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69a5e-108">EXAMPLES</span></span>

### <span data-ttu-id="69a5e-109">Örnek 1: esnek bir havuzun işlemlerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="69a5e-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="69a5e-110">Bu komut, ElasticPool01 adlı esnek havuz işlemlerinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="69a5e-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="69a5e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69a5e-111">PARAMETERS</span></span>

### <span data-ttu-id="69a5e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a5e-112">-DefaultProfile</span></span>
<span data-ttu-id="69a5e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69a5e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69a5e-114">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="69a5e-114">-ElasticPoolName</span></span>
<span data-ttu-id="69a5e-115">Esnek bir havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a5e-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="69a5e-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="69a5e-116">-OperationId</span></span>
<span data-ttu-id="69a5e-117">Alınacak işlemin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="69a5e-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="69a5e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a5e-118">-ResourceGroupName</span></span>
<span data-ttu-id="69a5e-119">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a5e-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="69a5e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69a5e-120">-ServerName</span></span>
<span data-ttu-id="69a5e-121">Elastik havuz içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69a5e-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="69a5e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="69a5e-122">-Confirm</span></span>
<span data-ttu-id="69a5e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69a5e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a5e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a5e-124">-WhatIf</span></span>
<span data-ttu-id="69a5e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69a5e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a5e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69a5e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a5e-127">CommonParameters</span></span>
<span data-ttu-id="69a5e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69a5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a5e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a5e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a5e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69a5e-130">INPUTS</span></span>

### <span data-ttu-id="69a5e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="69a5e-131">System.String</span></span>

### <span data-ttu-id="69a5e-132">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="69a5e-132">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="69a5e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69a5e-133">OUTPUTS</span></span>

### <span data-ttu-id="69a5e-134">Microsoft. Azure. Commands. Sql. Elaçıkartma. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="69a5e-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="69a5e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69a5e-135">NOTES</span></span>

## <span data-ttu-id="69a5e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69a5e-136">RELATED LINKS</span></span>

[<span data-ttu-id="69a5e-137">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="69a5e-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="69a5e-138">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="69a5e-138">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="69a5e-139">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="69a5e-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="69a5e-140">Remove-Azurermsqlelaunpool</span><span class="sxs-lookup"><span data-stu-id="69a5e-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="69a5e-141">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="69a5e-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


