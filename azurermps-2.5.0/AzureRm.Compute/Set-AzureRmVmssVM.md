---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940170"
---
# <span data-ttu-id="a1dbf-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a1dbf-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="a1dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="a1dbf-103">Bir VMSS örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1dbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1dbf-104">SYNTAX</span></span>

### <span data-ttu-id="a1dbf-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1dbf-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1dbf-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="a1dbf-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1dbf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1dbf-107">DESCRIPTION</span></span>
<span data-ttu-id="a1dbf-108">**Set-AzureRmVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a1dbf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1dbf-109">EXAMPLES</span></span>

## <span data-ttu-id="a1dbf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1dbf-110">PARAMETERS</span></span>

### <span data-ttu-id="a1dbf-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a1dbf-111">-AsJob</span></span>
<span data-ttu-id="a1dbf-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a1dbf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1dbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dbf-113">-DefaultProfile</span></span>
<span data-ttu-id="a1dbf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1dbf-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a1dbf-115">-InstanceId</span></span>
<span data-ttu-id="a1dbf-116">Bu cmdlet 'in durumu değiştirdiği VMSS örneğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1dbf-117">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="a1dbf-117">-Reimage</span></span>
<span data-ttu-id="a1dbf-118">Bu cmdlet 'in VMSS örneğini yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1dbf-119">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="a1dbf-119">-ReimageAll</span></span>
<span data-ttu-id="a1dbf-120">Cmdlet 'in VMSS örneğindeki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1dbf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1dbf-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1dbf-122">VMSS örneğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="a1dbf-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a1dbf-123">-VMScaleSetName</span></span>
<span data-ttu-id="a1dbf-124">Bu cmdlet 'in değiştirdiği VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a1dbf-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1dbf-125">-Confirm</span></span>
<span data-ttu-id="a1dbf-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1dbf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1dbf-127">-WhatIf</span></span>
<span data-ttu-id="a1dbf-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1dbf-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1dbf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dbf-130">CommonParameters</span></span>
<span data-ttu-id="a1dbf-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dbf-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1dbf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dbf-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1dbf-133">INPUTS</span></span>

### <span data-ttu-id="a1dbf-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1dbf-134">None</span></span>
<span data-ttu-id="a1dbf-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a1dbf-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1dbf-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1dbf-136">OUTPUTS</span></span>

### <span data-ttu-id="a1dbf-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="a1dbf-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a1dbf-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1dbf-138">NOTES</span></span>

## <span data-ttu-id="a1dbf-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1dbf-139">RELATED LINKS</span></span>

[<span data-ttu-id="a1dbf-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="a1dbf-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
