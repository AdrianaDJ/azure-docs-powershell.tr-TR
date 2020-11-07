---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938887"
---
# <span data-ttu-id="a2d2b-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a2d2b-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="a2d2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d2b-103">Bir uzantıyı VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2d2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2d2b-104">SYNTAX</span></span>

### <span data-ttu-id="a2d2b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2d2b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d2b-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="a2d2b-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d2b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2d2b-107">DESCRIPTION</span></span>
<span data-ttu-id="a2d2b-108">**Remove-Azurermvmssextenma** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a2d2b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2d2b-109">EXAMPLES</span></span>

## <span data-ttu-id="a2d2b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2d2b-110">PARAMETERS</span></span>

### <span data-ttu-id="a2d2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d2b-111">-DefaultProfile</span></span>
<span data-ttu-id="a2d2b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d2b-113">-ID</span><span class="sxs-lookup"><span data-stu-id="a2d2b-113">-Id</span></span>
<span data-ttu-id="a2d2b-114">Bu cmdlet 'in VMSUBNET 'den kaldırdığı uzantının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d2b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2d2b-115">-Name</span></span>
<span data-ttu-id="a2d2b-116">Bu cmdlet 'in kaldırıldığı uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d2b-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a2d2b-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a2d2b-118">Uzantısının kaldırılacağı VMSS 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-118">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d2b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2d2b-119">-Confirm</span></span>
<span data-ttu-id="a2d2b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d2b-121">-WhatIf</span></span>
<span data-ttu-id="a2d2b-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2d2b-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d2b-124">CommonParameters</span></span>
<span data-ttu-id="a2d2b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d2b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d2b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2d2b-127">INPUTS</span></span>

### <span data-ttu-id="a2d2b-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a2d2b-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a2d2b-129">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a2d2b-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a2d2b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2d2b-130">OUTPUTS</span></span>

### <span data-ttu-id="a2d2b-131">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a2d2b-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a2d2b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2d2b-132">NOTES</span></span>

## <span data-ttu-id="a2d2b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2d2b-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2d2b-134">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="a2d2b-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
