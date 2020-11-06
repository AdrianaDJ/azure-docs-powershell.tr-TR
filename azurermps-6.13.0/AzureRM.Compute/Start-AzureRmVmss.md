---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572878"
---
# <span data-ttu-id="a2b03-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="a2b03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b03-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b03-103">VMSS 'yi veya VMSS içinde bir dizi sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="a2b03-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2b03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2b03-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2b03-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b03-106">**Start-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="a2b03-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="a2b03-107">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2b03-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="a2b03-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2b03-108">EXAMPLES</span></span>

### <span data-ttu-id="a2b03-109">Örnek 1: VMSS içinde belirli bir sanal makine kümesini başlatma</span><span class="sxs-lookup"><span data-stu-id="a2b03-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="a2b03-110">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a2b03-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="a2b03-111">Örnek 2: VMSS içindeki tüm sanal makineleri başlatma</span><span class="sxs-lookup"><span data-stu-id="a2b03-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a2b03-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="a2b03-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a2b03-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2b03-113">PARAMETERS</span></span>

### <span data-ttu-id="a2b03-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a2b03-114">-AsJob</span></span>
<span data-ttu-id="a2b03-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="a2b03-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b03-116">-DefaultProfile</span></span>
<span data-ttu-id="a2b03-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2b03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b03-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a2b03-118">-InstanceId</span></span>
<span data-ttu-id="a2b03-119">Cmdlet 'in başladığı örneklerin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2b03-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="a2b03-120">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="a2b03-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b03-121">-ResourceGroupName</span></span>
<span data-ttu-id="a2b03-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2b03-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a2b03-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a2b03-123">-VMScaleSetName</span></span>
<span data-ttu-id="a2b03-124">Bu cmdlet 'in sanal makineleri Başlatan VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2b03-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="a2b03-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2b03-125">-Confirm</span></span>
<span data-ttu-id="a2b03-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2b03-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b03-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b03-127">-WhatIf</span></span>
<span data-ttu-id="a2b03-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2b03-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2b03-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2b03-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b03-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b03-130">CommonParameters</span></span>
<span data-ttu-id="a2b03-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2b03-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b03-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b03-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b03-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2b03-133">INPUTS</span></span>

### <span data-ttu-id="a2b03-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a2b03-134">System.String</span></span>

### <span data-ttu-id="a2b03-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="a2b03-135">System.String[]</span></span>

## <span data-ttu-id="a2b03-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2b03-136">OUTPUTS</span></span>

### <span data-ttu-id="a2b03-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="a2b03-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a2b03-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2b03-138">NOTES</span></span>

## <span data-ttu-id="a2b03-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2b03-139">RELATED LINKS</span></span>

[<span data-ttu-id="a2b03-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a2b03-141">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a2b03-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a2b03-143">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a2b03-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a2b03-145">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a2b03-146">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a2b03-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


