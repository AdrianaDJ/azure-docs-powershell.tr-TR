---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106447"
---
# <span data-ttu-id="28ada-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="28ada-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="28ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ada-102">SYNOPSIS</span></span>
<span data-ttu-id="28ada-103">Bir sanal makineden Azure DSC uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28ada-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="28ada-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28ada-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28ada-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28ada-105">DESCRIPTION</span></span>
<span data-ttu-id="28ada-106">**Remove-AzureVMDscExtension** cmdlet 'i, BIR Azure DSC uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28ada-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="28ada-107">Bu cmdlet 'in çıkışının **Update-AzureVM** cmdlet 'ine yöneltilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="28ada-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="28ada-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28ada-108">EXAMPLES</span></span>

### <span data-ttu-id="28ada-109">Örnek 1: bir sanal makineden DSC uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="28ada-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="28ada-110">Bu komut, bir sanal makineden Azure DSC uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="28ada-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="28ada-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28ada-111">PARAMETERS</span></span>

### <span data-ttu-id="28ada-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="28ada-112">-InformationAction</span></span>
<span data-ttu-id="28ada-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28ada-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="28ada-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="28ada-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28ada-115">'A</span><span class="sxs-lookup"><span data-stu-id="28ada-115">Continue</span></span>
- <span data-ttu-id="28ada-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="28ada-116">Ignore</span></span>
- <span data-ttu-id="28ada-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="28ada-117">Inquire</span></span>
- <span data-ttu-id="28ada-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="28ada-118">SilentlyContinue</span></span>
- <span data-ttu-id="28ada-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="28ada-119">Stop</span></span>
- <span data-ttu-id="28ada-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="28ada-120">Suspend</span></span>

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

### <span data-ttu-id="28ada-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="28ada-121">-InformationVariable</span></span>
<span data-ttu-id="28ada-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="28ada-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="28ada-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="28ada-123">-Profile</span></span>
<span data-ttu-id="28ada-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28ada-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28ada-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="28ada-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28ada-126">-VM</span><span class="sxs-lookup"><span data-stu-id="28ada-126">-VM</span></span>
<span data-ttu-id="28ada-127">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="28ada-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="28ada-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="28ada-128">-Confirm</span></span>
<span data-ttu-id="28ada-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28ada-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ada-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28ada-130">-WhatIf</span></span>
<span data-ttu-id="28ada-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28ada-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28ada-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28ada-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ada-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ada-133">CommonParameters</span></span>
<span data-ttu-id="28ada-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28ada-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ada-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ada-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ada-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28ada-136">INPUTS</span></span>

## <span data-ttu-id="28ada-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28ada-137">OUTPUTS</span></span>

## <span data-ttu-id="28ada-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28ada-138">NOTES</span></span>

## <span data-ttu-id="28ada-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28ada-139">RELATED LINKS</span></span>

[<span data-ttu-id="28ada-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="28ada-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="28ada-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="28ada-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="28ada-142">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="28ada-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


