---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 2e878c562c8f60ecebc9b6a43b3980e06fd0e355
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097200"
---
# <span data-ttu-id="d6728-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d6728-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="d6728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6728-102">SYNOPSIS</span></span>
<span data-ttu-id="d6728-103">Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulama türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d6728-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="d6728-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6728-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6728-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6728-105">DESCRIPTION</span></span>
<span data-ttu-id="d6728-106">Cmdlet, belirtilen kaynak grubu ve küme altında yeni bir hizmet yapısı uygulaması türü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6728-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="d6728-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6728-107">EXAMPLES</span></span>

### <span data-ttu-id="d6728-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6728-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="d6728-109">Bu örnek, kaynak grubunun ve kümenin altındaki "testAppType" yeni bir uygulama türü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6728-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="d6728-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6728-110">PARAMETERS</span></span>

### <span data-ttu-id="d6728-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d6728-111">-ClusterName</span></span>
<span data-ttu-id="d6728-112">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d6728-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d6728-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6728-113">-DefaultProfile</span></span>
<span data-ttu-id="d6728-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6728-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6728-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6728-115">-Name</span></span>
<span data-ttu-id="d6728-116">Uygulama türünün adını belirtme</span><span class="sxs-lookup"><span data-stu-id="d6728-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6728-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6728-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6728-118">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d6728-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d6728-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6728-119">-Confirm</span></span>
<span data-ttu-id="d6728-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6728-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6728-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6728-121">-WhatIf</span></span>
<span data-ttu-id="d6728-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6728-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6728-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6728-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6728-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6728-124">CommonParameters</span></span>
<span data-ttu-id="d6728-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6728-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6728-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6728-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6728-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6728-127">INPUTS</span></span>

### <span data-ttu-id="d6728-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d6728-128">System.String</span></span>

## <span data-ttu-id="d6728-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6728-129">OUTPUTS</span></span>

### <span data-ttu-id="d6728-130">Microsoft. Azure. Commands. ServiceFabric. modeller. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="d6728-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="d6728-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6728-131">NOTES</span></span>

## <span data-ttu-id="d6728-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6728-132">RELATED LINKS</span></span>
