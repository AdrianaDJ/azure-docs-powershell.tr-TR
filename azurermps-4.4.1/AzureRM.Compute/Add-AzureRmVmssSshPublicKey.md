---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 113af7a35ffee5960f4be6fe2fe989d9c1b36956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593583"
---
# <span data-ttu-id="6077b-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6077b-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="6077b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6077b-102">SYNOPSIS</span></span>
<span data-ttu-id="6077b-103">VMSS 'ye SSH ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="6077b-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6077b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6077b-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6077b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6077b-105">DESCRIPTION</span></span>
<span data-ttu-id="6077b-106">**Add-AzureRmVmssSshPublicKey** cmdlet 'ı güvenli kabukta (SSH) sanal makine ölçek KÜMESI (VMSS) sanal makinelerine bağlamak için kullanabileceğiniz ortak anahtarları ekler.</span><span class="sxs-lookup"><span data-stu-id="6077b-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="6077b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6077b-107">EXAMPLES</span></span>

### <span data-ttu-id="6077b-108">Örnek 1: VMSS 'ye SSH ortak anahtarı ekleme</span><span class="sxs-lookup"><span data-stu-id="6077b-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="6077b-109">Bu örnek, VMSS 'ye bir SSH ortak anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="6077b-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="6077b-110">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6077b-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="6077b-111">İkinci komut, belirtilen anahtar verilerine sahip bir SSH anahtarı ekler ve anahtarı sanal makinedeki belirtilen yolda depolar.</span><span class="sxs-lookup"><span data-stu-id="6077b-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="6077b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6077b-112">PARAMETERS</span></span>

### <span data-ttu-id="6077b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6077b-113">-DefaultProfile</span></span>
<span data-ttu-id="6077b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6077b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6077b-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="6077b-115">-KeyData</span></span>
<span data-ttu-id="6077b-116">SSH RSA ortak anahtar verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6077b-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="6077b-117">-Yol</span><span class="sxs-lookup"><span data-stu-id="6077b-117">-Path</span></span>
<span data-ttu-id="6077b-118">Sanal makinede, bu cmdlet 'in SSH ortak anahtarını sakladığı bir dosyanın tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6077b-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="6077b-119">Dosya zaten varsa, bu cmdlet anahtarı dosyaya ekler.</span><span class="sxs-lookup"><span data-stu-id="6077b-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="6077b-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6077b-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6077b-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6077b-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="6077b-122">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6077b-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6077b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="6077b-123">-Confirm</span></span>
<span data-ttu-id="6077b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6077b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6077b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6077b-125">-WhatIf</span></span>
<span data-ttu-id="6077b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6077b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6077b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6077b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6077b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6077b-128">CommonParameters</span></span>
<span data-ttu-id="6077b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6077b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6077b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6077b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6077b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6077b-131">INPUTS</span></span>

## <span data-ttu-id="6077b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6077b-132">OUTPUTS</span></span>

###  
<span data-ttu-id="6077b-133">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6077b-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6077b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6077b-134">NOTES</span></span>

## <span data-ttu-id="6077b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6077b-135">RELATED LINKS</span></span>

[<span data-ttu-id="6077b-136">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6077b-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
