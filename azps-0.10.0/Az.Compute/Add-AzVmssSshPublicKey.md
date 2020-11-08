---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 2fb8d5956cf783940e32f49019115dd911050749
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937076"
---
# <span data-ttu-id="e352b-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e352b-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="e352b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e352b-102">SYNOPSIS</span></span>
<span data-ttu-id="e352b-103">VMSS 'ye SSH ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="e352b-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="e352b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e352b-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e352b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e352b-105">DESCRIPTION</span></span>
<span data-ttu-id="e352b-106">**Add-AzVmssSshPublicKey** cmdlet 'ı güvenli kabukta (SSH) sanal makine ölçek KÜMESI (VMSS) sanal makinelerine bağlamak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="e352b-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="e352b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e352b-107">EXAMPLES</span></span>

### <span data-ttu-id="e352b-108">Örnek 1: VMSS 'ye SSH ortak anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="e352b-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="e352b-109">Bu örnek, VMSS 'ye bir SSH ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="e352b-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="e352b-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="e352b-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e352b-111">İkinci komut, belirtilen anahtar verilerine sahip bir SSH anahtarı ekler ve anahtarı sanal makinedeki belirtilen yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="e352b-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="e352b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e352b-112">PARAMETERS</span></span>

### <span data-ttu-id="e352b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e352b-113">-DefaultProfile</span></span>
<span data-ttu-id="e352b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e352b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e352b-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="e352b-115">-KeyData</span></span>
<span data-ttu-id="e352b-116">SSH RSA ortak anahtar verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e352b-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="e352b-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="e352b-117">-Path</span></span>
<span data-ttu-id="e352b-118">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e352b-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="e352b-119">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="e352b-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="e352b-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e352b-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e352b-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e352b-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="e352b-122">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e352b-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e352b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e352b-123">-Confirm</span></span>
<span data-ttu-id="e352b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e352b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e352b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e352b-125">-WhatIf</span></span>
<span data-ttu-id="e352b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e352b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e352b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e352b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e352b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e352b-128">CommonParameters</span></span>
<span data-ttu-id="e352b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e352b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e352b-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e352b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e352b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e352b-131">INPUTS</span></span>

### <span data-ttu-id="e352b-132">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e352b-132">VirtualMachineScaleSet</span></span>
<span data-ttu-id="e352b-133">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e352b-133">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="e352b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e352b-134">OUTPUTS</span></span>

###  
<span data-ttu-id="e352b-135">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e352b-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e352b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e352b-136">NOTES</span></span>

## <span data-ttu-id="e352b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e352b-137">RELATED LINKS</span></span>

[<span data-ttu-id="e352b-138">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e352b-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)