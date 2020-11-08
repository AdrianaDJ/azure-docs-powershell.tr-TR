---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: d8fb3b740a85b4cb258fcfa08bf9f4e06032fcb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935932"
---
# <span data-ttu-id="70bbf-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="70bbf-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="70bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="70bbf-103">VMSS örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="70bbf-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="70bbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70bbf-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70bbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="70bbf-106">Update-AzVmssInstance cmdlet 'i, belirtilen sanal makine ölçek kümesi (VMSS) örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="70bbf-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="70bbf-107">Bu, VMSS ölçek kümesindeki yükseltme ilkesi el ile olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70bbf-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="70bbf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70bbf-108">EXAMPLES</span></span>

### <span data-ttu-id="70bbf-109">Örnek 1: VMSS örneğinin yükseltmesini başlatma</span><span class="sxs-lookup"><span data-stu-id="70bbf-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="70bbf-110">Bu komut, VMScaleSet001 adında, örnek KIMLIĞI 0 olan bir yükseltme başlatır.</span><span class="sxs-lookup"><span data-stu-id="70bbf-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="70bbf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70bbf-111">PARAMETERS</span></span>

### <span data-ttu-id="70bbf-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="70bbf-112">-AsJob</span></span>
<span data-ttu-id="70bbf-113">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="70bbf-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="70bbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bbf-114">-DefaultProfile</span></span>
<span data-ttu-id="70bbf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70bbf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70bbf-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="70bbf-116">-InstanceId</span></span>
<span data-ttu-id="70bbf-117">Bir dize dizisi, Yükseltilecek olan Örneğin KIMLIĞINI veya kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bbf-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70bbf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bbf-118">-ResourceGroupName</span></span>
<span data-ttu-id="70bbf-119">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bbf-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="70bbf-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="70bbf-120">-VMScaleSetName</span></span>
<span data-ttu-id="70bbf-121">Bu cmdlet 'in yükseltmelerine sahip VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="70bbf-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="70bbf-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="70bbf-122">-Confirm</span></span>
<span data-ttu-id="70bbf-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70bbf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70bbf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70bbf-124">-WhatIf</span></span>
<span data-ttu-id="70bbf-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70bbf-125">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="70bbf-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70bbf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70bbf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bbf-127">CommonParameters</span></span>
<span data-ttu-id="70bbf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70bbf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bbf-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bbf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bbf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70bbf-130">INPUTS</span></span>

### <span data-ttu-id="70bbf-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70bbf-131">None</span></span>
<span data-ttu-id="70bbf-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="70bbf-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70bbf-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70bbf-133">OUTPUTS</span></span>

###  
<span data-ttu-id="70bbf-134">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="70bbf-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="70bbf-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70bbf-135">NOTES</span></span>

## <span data-ttu-id="70bbf-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70bbf-136">RELATED LINKS</span></span>

[<span data-ttu-id="70bbf-137">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="70bbf-137">Update-AzVmss</span></span>](./Update-AzVmss.md)

