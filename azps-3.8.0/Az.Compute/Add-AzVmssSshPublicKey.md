---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104893"
---
# <span data-ttu-id="45d78-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="45d78-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="45d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d78-102">SYNOPSIS</span></span>
<span data-ttu-id="45d78-103">VMSS 'ye SSH ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="45d78-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="45d78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45d78-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45d78-105">DESCRIPTION</span></span>
<span data-ttu-id="45d78-106">**Add-AzVmssSshPublicKey** cmdlet 'ı güvenli kabukta (SSH) sanal makine ölçek KÜMESI (VMSS) sanal makinelerine bağlamak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="45d78-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="45d78-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45d78-107">EXAMPLES</span></span>

### <span data-ttu-id="45d78-108">Örnek 1: VMSS 'ye SSH ortak anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="45d78-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="45d78-109">Bu örnek, VMSS 'ye bir SSH ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="45d78-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="45d78-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="45d78-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="45d78-111">İkinci komut, belirtilen anahtar verilerine sahip bir SSH anahtarı ekler ve anahtarı sanal makinedeki belirtilen yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="45d78-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="45d78-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45d78-112">PARAMETERS</span></span>

### <span data-ttu-id="45d78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d78-113">-DefaultProfile</span></span>
<span data-ttu-id="45d78-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45d78-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d78-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="45d78-115">-KeyData</span></span>
<span data-ttu-id="45d78-116">SSH RSA ortak anahtar verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d78-116">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d78-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="45d78-117">-Path</span></span>
<span data-ttu-id="45d78-118">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d78-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="45d78-119">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="45d78-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d78-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="45d78-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="45d78-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d78-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="45d78-122">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="45d78-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45d78-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="45d78-123">-Confirm</span></span>
<span data-ttu-id="45d78-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45d78-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d78-125">-WhatIf</span></span>
<span data-ttu-id="45d78-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45d78-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45d78-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45d78-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d78-128">CommonParameters</span></span>
<span data-ttu-id="45d78-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45d78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d78-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45d78-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d78-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45d78-131">INPUTS</span></span>

### <span data-ttu-id="45d78-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="45d78-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="45d78-133">System. String</span><span class="sxs-lookup"><span data-stu-id="45d78-133">System.String</span></span>

## <span data-ttu-id="45d78-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45d78-134">OUTPUTS</span></span>

### <span data-ttu-id="45d78-135">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="45d78-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="45d78-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45d78-136">NOTES</span></span>

## <span data-ttu-id="45d78-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45d78-137">RELATED LINKS</span></span>

[<span data-ttu-id="45d78-138">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="45d78-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
