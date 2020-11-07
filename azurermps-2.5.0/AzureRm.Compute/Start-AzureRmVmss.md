---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939932"
---
# <span data-ttu-id="c7d10-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="c7d10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d10-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d10-103">VMSS 'yi veya VMSS içinde bir dizi sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="c7d10-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7d10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7d10-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7d10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7d10-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d10-106">**Start-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="c7d10-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c7d10-107">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7d10-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c7d10-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7d10-108">EXAMPLES</span></span>

### <span data-ttu-id="c7d10-109">Örnek 1: VMSS içinde belirli bir sanal makine kümesini başlatma</span><span class="sxs-lookup"><span data-stu-id="c7d10-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="c7d10-110">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c7d10-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c7d10-111">Örnek 2: VMSS içindeki tüm sanal makineleri başlatma</span><span class="sxs-lookup"><span data-stu-id="c7d10-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c7d10-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="c7d10-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c7d10-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7d10-113">PARAMETERS</span></span>

### <span data-ttu-id="c7d10-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="c7d10-114">-AsJob</span></span>
<span data-ttu-id="c7d10-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="c7d10-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c7d10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d10-116">-DefaultProfile</span></span>
<span data-ttu-id="c7d10-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7d10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d10-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c7d10-118">-InstanceId</span></span>
<span data-ttu-id="c7d10-119">Cmdlet 'in başladığı örneklerin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7d10-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="c7d10-120">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c7d10-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d10-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d10-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7d10-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7d10-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c7d10-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c7d10-123">-VMScaleSetName</span></span>
<span data-ttu-id="c7d10-124">Bu cmdlet 'in sanal makineleri Başlatan VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7d10-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="c7d10-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7d10-125">-Confirm</span></span>
<span data-ttu-id="c7d10-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7d10-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7d10-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7d10-127">-WhatIf</span></span>
<span data-ttu-id="c7d10-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7d10-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7d10-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7d10-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7d10-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d10-130">CommonParameters</span></span>
<span data-ttu-id="c7d10-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7d10-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d10-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d10-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d10-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7d10-133">INPUTS</span></span>

### <span data-ttu-id="c7d10-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c7d10-134">None</span></span>
<span data-ttu-id="c7d10-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c7d10-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7d10-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7d10-136">OUTPUTS</span></span>

###  
<span data-ttu-id="c7d10-137">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c7d10-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c7d10-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7d10-138">NOTES</span></span>

## <span data-ttu-id="c7d10-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7d10-139">RELATED LINKS</span></span>

[<span data-ttu-id="c7d10-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c7d10-141">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c7d10-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c7d10-143">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c7d10-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c7d10-145">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c7d10-146">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c7d10-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


