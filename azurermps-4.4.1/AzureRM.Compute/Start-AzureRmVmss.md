---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 6b3291a77f7c69372124b8c0de2ba78c8810f02b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763128"
---
# <span data-ttu-id="8030d-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="8030d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8030d-102">SYNOPSIS</span></span>
<span data-ttu-id="8030d-103">VMSS 'yi veya VMSS içinde bir dizi sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="8030d-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8030d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8030d-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8030d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8030d-105">DESCRIPTION</span></span>
<span data-ttu-id="8030d-106">**Start-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="8030d-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="8030d-107">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8030d-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="8030d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8030d-108">EXAMPLES</span></span>

### <span data-ttu-id="8030d-109">Örnek 1: VMSS içinde belirli bir sanal makine kümesini başlatma</span><span class="sxs-lookup"><span data-stu-id="8030d-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="8030d-110">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="8030d-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="8030d-111">Örnek 2: VMSS içindeki tüm sanal makineleri başlatma</span><span class="sxs-lookup"><span data-stu-id="8030d-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8030d-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="8030d-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="8030d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8030d-113">PARAMETERS</span></span>

### <span data-ttu-id="8030d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8030d-114">-DefaultProfile</span></span>
<span data-ttu-id="8030d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8030d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8030d-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8030d-116">-InstanceId</span></span>
<span data-ttu-id="8030d-117">Cmdlet 'in başladığı örneklerin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8030d-117">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="8030d-118">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="8030d-118">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="8030d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8030d-119">-ResourceGroupName</span></span>
<span data-ttu-id="8030d-120">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8030d-120">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="8030d-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8030d-121">-VMScaleSetName</span></span>
<span data-ttu-id="8030d-122">Bu cmdlet 'in sanal makineleri Başlatan VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8030d-122">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="8030d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="8030d-123">-Confirm</span></span>
<span data-ttu-id="8030d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8030d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8030d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8030d-125">-WhatIf</span></span>
<span data-ttu-id="8030d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8030d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8030d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8030d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8030d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8030d-128">CommonParameters</span></span>
<span data-ttu-id="8030d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8030d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8030d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8030d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8030d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8030d-131">INPUTS</span></span>

## <span data-ttu-id="8030d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8030d-132">OUTPUTS</span></span>

###  
<span data-ttu-id="8030d-133">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8030d-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8030d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8030d-134">NOTES</span></span>

## <span data-ttu-id="8030d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8030d-135">RELATED LINKS</span></span>

[<span data-ttu-id="8030d-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="8030d-137">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="8030d-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="8030d-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="8030d-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="8030d-141">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="8030d-142">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8030d-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)

