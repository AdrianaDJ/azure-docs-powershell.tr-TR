---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939768"
---
# <span data-ttu-id="c9868-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c9868-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="c9868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9868-102">SYNOPSIS</span></span>
<span data-ttu-id="c9868-103">Kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9868-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9868-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9868-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9868-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9868-105">DESCRIPTION</span></span>
<span data-ttu-id="c9868-106">**Remove-AzureRmContainerService** cmdlet 'i Azure hesabınızdan bir kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9868-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="c9868-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9868-107">EXAMPLES</span></span>

### <span data-ttu-id="c9868-108">Örnek 1: kapsayıcı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="c9868-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="c9868-109">Bu komut, CSResourceGroup17 adlı kapsayıcı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9868-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="c9868-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9868-110">PARAMETERS</span></span>

### <span data-ttu-id="c9868-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="c9868-111">-AsJob</span></span>
<span data-ttu-id="c9868-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="c9868-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c9868-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9868-113">-DefaultProfile</span></span>
<span data-ttu-id="c9868-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9868-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9868-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c9868-115">-Force</span></span>
<span data-ttu-id="c9868-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c9868-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9868-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9868-117">-Name</span></span>
<span data-ttu-id="c9868-118">Bu cmdlet 'in kaldırdığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9868-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9868-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9868-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9868-120">Bu cmdlet 'in kaldırdığı kapsayıcı hizmetin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9868-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9868-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9868-121">-Confirm</span></span>
<span data-ttu-id="c9868-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9868-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="c9868-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9868-123">-WhatIf</span></span>
<span data-ttu-id="c9868-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9868-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9868-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9868-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="c9868-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9868-126">CommonParameters</span></span>
<span data-ttu-id="c9868-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9868-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9868-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9868-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9868-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9868-129">INPUTS</span></span>

### <span data-ttu-id="c9868-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c9868-130">None</span></span>
<span data-ttu-id="c9868-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c9868-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9868-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9868-132">OUTPUTS</span></span>

### <span data-ttu-id="c9868-133">System. void</span><span class="sxs-lookup"><span data-stu-id="c9868-133">System.Void</span></span>

## <span data-ttu-id="c9868-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9868-134">NOTES</span></span>

## <span data-ttu-id="c9868-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9868-135">RELATED LINKS</span></span>

[<span data-ttu-id="c9868-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c9868-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="c9868-137">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c9868-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="c9868-138">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c9868-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


