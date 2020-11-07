---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764487"
---
# <span data-ttu-id="499a7-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="499a7-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="499a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="499a7-102">SYNOPSIS</span></span>
<span data-ttu-id="499a7-103">VMSS 'ye SSH ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="499a7-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="499a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="499a7-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="499a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="499a7-105">DESCRIPTION</span></span>
<span data-ttu-id="499a7-106">**Add-AzureRmVmssSshPublicKey** cmdlet 'ı güvenli kabukta (SSH) sanal makine ölçek KÜMESI (VMSS) sanal makinelerine bağlamak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="499a7-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="499a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="499a7-107">EXAMPLES</span></span>

### <span data-ttu-id="499a7-108">Örnek 1: VMSS 'ye SSH ortak anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="499a7-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="499a7-109">Bu örnek, VMSS 'ye bir SSH ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="499a7-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="499a7-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="499a7-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="499a7-111">İkinci komut, belirtilen anahtar verilerine sahip bir SSH anahtarı ekler ve anahtarı sanal makinedeki belirtilen yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="499a7-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="499a7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="499a7-112">PARAMETERS</span></span>

### <span data-ttu-id="499a7-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="499a7-113">-KeyData</span></span>
<span data-ttu-id="499a7-114">SSH RSA ortak anahtar verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="499a7-114">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a7-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="499a7-115">-Path</span></span>
<span data-ttu-id="499a7-116">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="499a7-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="499a7-117">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="499a7-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499a7-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="499a7-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="499a7-119">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="499a7-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="499a7-120">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="499a7-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="499a7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="499a7-121">-Confirm</span></span>
<span data-ttu-id="499a7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="499a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="499a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="499a7-123">-WhatIf</span></span>
<span data-ttu-id="499a7-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="499a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="499a7-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="499a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="499a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499a7-126">CommonParameters</span></span>
<span data-ttu-id="499a7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="499a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499a7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="499a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499a7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="499a7-129">INPUTS</span></span>

### <span data-ttu-id="499a7-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="499a7-130">None</span></span>
<span data-ttu-id="499a7-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="499a7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="499a7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="499a7-132">OUTPUTS</span></span>

###  
<span data-ttu-id="499a7-133">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="499a7-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="499a7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="499a7-134">NOTES</span></span>

## <span data-ttu-id="499a7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="499a7-135">RELATED LINKS</span></span>

[<span data-ttu-id="499a7-136">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="499a7-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
