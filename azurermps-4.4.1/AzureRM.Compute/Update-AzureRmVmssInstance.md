---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 1d7655a78ee2abe00b69d485c35b73cee91ee420
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762708"
---
# <span data-ttu-id="0b867-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="0b867-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="0b867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b867-102">SYNOPSIS</span></span>
<span data-ttu-id="0b867-103">VMSS örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="0b867-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b867-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b867-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b867-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b867-105">DESCRIPTION</span></span>
<span data-ttu-id="0b867-106">Update-AzureRmVmssInstance cmdlet 'i, belirtilen sanal makine ölçek kümesi (VMSS) örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="0b867-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="0b867-107">Bu, VMSS ölçek kümesindeki yükseltme ilkesi el ile olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b867-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="0b867-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b867-108">EXAMPLES</span></span>

### <span data-ttu-id="0b867-109">Örnek 1: VMSS örneğinin yükseltmesini başlatma</span><span class="sxs-lookup"><span data-stu-id="0b867-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="0b867-110">Bu komut, VMScaleSet001 adında, örnek KIMLIĞI 0 olan bir yükseltme başlatır.</span><span class="sxs-lookup"><span data-stu-id="0b867-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="0b867-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b867-111">PARAMETERS</span></span>

### <span data-ttu-id="0b867-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b867-112">-DefaultProfile</span></span>
<span data-ttu-id="0b867-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b867-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b867-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0b867-114">-InstanceId</span></span>
<span data-ttu-id="0b867-115">Bir dize dizisi, Yükseltilecek olan Örneğin KIMLIĞINI veya kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b867-115">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b867-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b867-116">-ResourceGroupName</span></span>
<span data-ttu-id="0b867-117">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b867-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0b867-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0b867-118">-VMScaleSetName</span></span>
<span data-ttu-id="0b867-119">Bu cmdlet 'in yükseltmelerine sahip VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b867-119">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="0b867-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b867-120">-Confirm</span></span>
<span data-ttu-id="0b867-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b867-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b867-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b867-122">-WhatIf</span></span>
<span data-ttu-id="0b867-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b867-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0b867-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b867-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b867-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b867-125">CommonParameters</span></span>
<span data-ttu-id="0b867-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b867-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b867-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b867-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b867-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b867-128">INPUTS</span></span>

## <span data-ttu-id="0b867-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b867-129">OUTPUTS</span></span>

###  
<span data-ttu-id="0b867-130">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0b867-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0b867-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b867-131">NOTES</span></span>

## <span data-ttu-id="0b867-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b867-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b867-133">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b867-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


