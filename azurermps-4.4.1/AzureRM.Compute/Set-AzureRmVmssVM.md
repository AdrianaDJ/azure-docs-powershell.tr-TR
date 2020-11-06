---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587997"
---
# <span data-ttu-id="170d6-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="170d6-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="170d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170d6-102">SYNOPSIS</span></span>
<span data-ttu-id="170d6-103">Bir VMSS örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="170d6-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="170d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="170d6-104">SYNTAX</span></span>

### <span data-ttu-id="170d6-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="170d6-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170d6-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="170d6-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170d6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="170d6-107">DESCRIPTION</span></span>
<span data-ttu-id="170d6-108">**Set-AzureRmVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) örneğinin durumunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="170d6-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="170d6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="170d6-109">EXAMPLES</span></span>

## <span data-ttu-id="170d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="170d6-110">PARAMETERS</span></span>

### <span data-ttu-id="170d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170d6-111">-DefaultProfile</span></span>
<span data-ttu-id="170d6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="170d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170d6-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="170d6-113">-InstanceId</span></span>
<span data-ttu-id="170d6-114">Bu cmdlet 'in durumu değiştirdiği VMSS örneğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="170d6-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170d6-115">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="170d6-115">-Reimage</span></span>
<span data-ttu-id="170d6-116">Bu cmdlet 'in VMSS örneğini yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="170d6-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170d6-117">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="170d6-117">-ReimageAll</span></span>
<span data-ttu-id="170d6-118">Cmdlet 'in VMSS örneğindeki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="170d6-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="170d6-120">VMSS örneğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170d6-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="170d6-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="170d6-121">-VMScaleSetName</span></span>
<span data-ttu-id="170d6-122">Bu cmdlet 'in değiştirdiği VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170d6-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="170d6-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="170d6-123">-Confirm</span></span>
<span data-ttu-id="170d6-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="170d6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170d6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170d6-125">-WhatIf</span></span>
<span data-ttu-id="170d6-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="170d6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="170d6-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="170d6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170d6-128">CommonParameters</span></span>
<span data-ttu-id="170d6-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="170d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170d6-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170d6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170d6-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="170d6-131">INPUTS</span></span>

## <span data-ttu-id="170d6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="170d6-132">OUTPUTS</span></span>

## <span data-ttu-id="170d6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="170d6-133">NOTES</span></span>

## <span data-ttu-id="170d6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="170d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="170d6-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="170d6-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
