---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106332"
---
# <span data-ttu-id="aac8d-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="aac8d-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="aac8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac8d-102">SYNOPSIS</span></span>
<span data-ttu-id="aac8d-103">Bir Azure sanal makinesinin işletim sistemi diskini alır.</span><span class="sxs-lookup"><span data-stu-id="aac8d-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="aac8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aac8d-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aac8d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aac8d-105">DESCRIPTION</span></span>
<span data-ttu-id="aac8d-106">**Get-AzureOSDisk** cmdlet 'ı bir Azure sanal makinesinin işletim sistemi diskini alır.</span><span class="sxs-lookup"><span data-stu-id="aac8d-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="aac8d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aac8d-107">EXAMPLES</span></span>

### <span data-ttu-id="aac8d-108">Örnek 1: işletim sistemi disketi edinme</span><span class="sxs-lookup"><span data-stu-id="aac8d-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="aac8d-109">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine02 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="aac8d-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="aac8d-110">Komut, ardışık düzen işlecini kullanarak sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="aac8d-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aac8d-111">Geçerli cmdlet, bu sanal makinenin işletim sistemi diskini alır.</span><span class="sxs-lookup"><span data-stu-id="aac8d-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="aac8d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aac8d-112">PARAMETERS</span></span>

### <span data-ttu-id="aac8d-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="aac8d-113">-InformationAction</span></span>
<span data-ttu-id="aac8d-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac8d-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aac8d-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aac8d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aac8d-116">'A</span><span class="sxs-lookup"><span data-stu-id="aac8d-116">Continue</span></span>
- <span data-ttu-id="aac8d-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="aac8d-117">Ignore</span></span>
- <span data-ttu-id="aac8d-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="aac8d-118">Inquire</span></span>
- <span data-ttu-id="aac8d-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="aac8d-119">SilentlyContinue</span></span>
- <span data-ttu-id="aac8d-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="aac8d-120">Stop</span></span>
- <span data-ttu-id="aac8d-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="aac8d-121">Suspend</span></span>

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

### <span data-ttu-id="aac8d-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="aac8d-122">-InformationVariable</span></span>
<span data-ttu-id="aac8d-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac8d-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aac8d-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="aac8d-124">-Profile</span></span>
<span data-ttu-id="aac8d-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac8d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aac8d-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="aac8d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac8d-127">-VM</span><span class="sxs-lookup"><span data-stu-id="aac8d-127">-VM</span></span>
<span data-ttu-id="aac8d-128">Bu cmdlet 'in işletim sistemi disketini aldığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac8d-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="aac8d-129">Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aac8d-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aac8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac8d-130">CommonParameters</span></span>
<span data-ttu-id="aac8d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aac8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac8d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac8d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac8d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aac8d-133">INPUTS</span></span>

## <span data-ttu-id="aac8d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aac8d-134">OUTPUTS</span></span>

## <span data-ttu-id="aac8d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aac8d-135">NOTES</span></span>

## <span data-ttu-id="aac8d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aac8d-136">RELATED LINKS</span></span>

[<span data-ttu-id="aac8d-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="aac8d-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="aac8d-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="aac8d-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


