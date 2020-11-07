---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssshpublickey
schema: 2.0.0
ms.openlocfilehash: 6cd715c3ba6ef0a890f5aaeaf04022b19026592c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939190"
---
# <span data-ttu-id="d916c-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d916c-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="d916c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d916c-102">SYNOPSIS</span></span>
<span data-ttu-id="d916c-103">VMSS 'ye SSH ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="d916c-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d916c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d916c-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d916c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d916c-105">DESCRIPTION</span></span>
<span data-ttu-id="d916c-106">**Add-AzureRmVmssSshPublicKey** cmdlet 'ı güvenli kabukta (SSH) sanal makine ölçek KÜMESI (VMSS) sanal makinelerine bağlamak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="d916c-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="d916c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d916c-107">EXAMPLES</span></span>

### <span data-ttu-id="d916c-108">Örnek 1: VMSS 'ye SSH ortak anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="d916c-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="d916c-109">Bu örnek, VMSS 'ye bir SSH ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="d916c-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="d916c-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d916c-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="d916c-111">İkinci komut, belirtilen anahtar verilerine sahip bir SSH anahtarı ekler ve anahtarı sanal makinedeki belirtilen yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="d916c-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="d916c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d916c-112">PARAMETERS</span></span>

### <span data-ttu-id="d916c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d916c-113">-DefaultProfile</span></span>
<span data-ttu-id="d916c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d916c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d916c-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="d916c-115">-KeyData</span></span>
<span data-ttu-id="d916c-116">SSH RSA ortak anahtar verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d916c-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="d916c-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="d916c-117">-Path</span></span>
<span data-ttu-id="d916c-118">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d916c-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="d916c-119">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="d916c-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="d916c-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d916c-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d916c-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d916c-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="d916c-122">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d916c-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d916c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d916c-123">-Confirm</span></span>
<span data-ttu-id="d916c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d916c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d916c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d916c-125">-WhatIf</span></span>
<span data-ttu-id="d916c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d916c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d916c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d916c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d916c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d916c-128">CommonParameters</span></span>
<span data-ttu-id="d916c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d916c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d916c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d916c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d916c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d916c-131">INPUTS</span></span>

### <span data-ttu-id="d916c-132">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d916c-132">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d916c-133">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d916c-133">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d916c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d916c-134">OUTPUTS</span></span>

###  
<span data-ttu-id="d916c-135">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d916c-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d916c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d916c-136">NOTES</span></span>

## <span data-ttu-id="d916c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d916c-137">RELATED LINKS</span></span>

[<span data-ttu-id="d916c-138">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d916c-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
