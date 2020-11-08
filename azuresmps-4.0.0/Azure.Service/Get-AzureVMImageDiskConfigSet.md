---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106530"
---
# <span data-ttu-id="ebd72-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ebd72-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="ebd72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd72-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd72-103">Giriş görüntü bağlamından bir disk yapılandırması kümesi nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="ebd72-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="ebd72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebd72-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ebd72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebd72-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd72-106">**Get-AzureVMImageDiskConfigSet** cmdlet 'i, giriş görüntü bağlamından bir disk yapılandırması kümesi nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="ebd72-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="ebd72-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebd72-107">EXAMPLES</span></span>

### <span data-ttu-id="ebd72-108">Örnek 1: sanal makineden bir disk yapılandırması kümesi nesnesi alma</span><span class="sxs-lookup"><span data-stu-id="ebd72-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="ebd72-109">Bu komut, bir sanal makineden bir disk yapılandırması kümesi nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="ebd72-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="ebd72-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebd72-110">PARAMETERS</span></span>

### <span data-ttu-id="ebd72-111">-Imagecontext</span><span class="sxs-lookup"><span data-stu-id="ebd72-111">-ImageContext</span></span>
<span data-ttu-id="ebd72-112">Sanal makine görüntü bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd72-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd72-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ebd72-113">-InformationAction</span></span>
<span data-ttu-id="ebd72-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd72-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ebd72-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ebd72-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ebd72-116">'A</span><span class="sxs-lookup"><span data-stu-id="ebd72-116">Continue</span></span>
- <span data-ttu-id="ebd72-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="ebd72-117">Ignore</span></span>
- <span data-ttu-id="ebd72-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ebd72-118">Inquire</span></span>
- <span data-ttu-id="ebd72-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ebd72-119">SilentlyContinue</span></span>
- <span data-ttu-id="ebd72-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ebd72-120">Stop</span></span>
- <span data-ttu-id="ebd72-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ebd72-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd72-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ebd72-122">-InformationVariable</span></span>
<span data-ttu-id="ebd72-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd72-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd72-124">CommonParameters</span></span>
<span data-ttu-id="ebd72-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebd72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd72-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd72-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd72-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebd72-127">INPUTS</span></span>

## <span data-ttu-id="ebd72-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebd72-128">OUTPUTS</span></span>

### <span data-ttu-id="ebd72-129">Microsoft. Windowsazde. Commands. ServiceManagement. model. Virtualmachineımagediskconfigset</span><span class="sxs-lookup"><span data-stu-id="ebd72-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="ebd72-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebd72-130">NOTES</span></span>

## <span data-ttu-id="ebd72-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebd72-131">RELATED LINKS</span></span>

[<span data-ttu-id="ebd72-132">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ebd72-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="ebd72-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ebd72-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


