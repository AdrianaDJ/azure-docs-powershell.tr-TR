---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105510"
---
# <span data-ttu-id="755a4-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="755a4-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="755a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755a4-102">SYNOPSIS</span></span>
<span data-ttu-id="755a4-103">Sanal makineye uygulanan VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="755a4-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="755a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="755a4-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="755a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="755a4-105">DESCRIPTION</span></span>
<span data-ttu-id="755a4-106">**Remove-AzureVMAccessExtension** cmdlet 'i, sanal makineye uygulanan VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="755a4-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="755a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="755a4-107">EXAMPLES</span></span>

### <span data-ttu-id="755a4-108">Örnek 1: sanal makineden VMAccess uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="755a4-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="755a4-109">Bu komut bir sanal makineden VMAccess uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="755a4-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="755a4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="755a4-110">PARAMETERS</span></span>

### <span data-ttu-id="755a4-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="755a4-111">-InformationAction</span></span>
<span data-ttu-id="755a4-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="755a4-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="755a4-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="755a4-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="755a4-114">'A</span><span class="sxs-lookup"><span data-stu-id="755a4-114">Continue</span></span>
- <span data-ttu-id="755a4-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="755a4-115">Ignore</span></span>
- <span data-ttu-id="755a4-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="755a4-116">Inquire</span></span>
- <span data-ttu-id="755a4-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="755a4-117">SilentlyContinue</span></span>
- <span data-ttu-id="755a4-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="755a4-118">Stop</span></span>
- <span data-ttu-id="755a4-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="755a4-119">Suspend</span></span>

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

### <span data-ttu-id="755a4-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="755a4-120">-InformationVariable</span></span>
<span data-ttu-id="755a4-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="755a4-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="755a4-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="755a4-122">-Profile</span></span>
<span data-ttu-id="755a4-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="755a4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="755a4-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="755a4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="755a4-125">-VM</span><span class="sxs-lookup"><span data-stu-id="755a4-125">-VM</span></span>
<span data-ttu-id="755a4-126">Bu cmdlet 'in VMAccess uzantısını kaldırdığı kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="755a4-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="755a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755a4-127">CommonParameters</span></span>
<span data-ttu-id="755a4-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="755a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755a4-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755a4-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="755a4-130">INPUTS</span></span>

## <span data-ttu-id="755a4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="755a4-131">OUTPUTS</span></span>

## <span data-ttu-id="755a4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="755a4-132">NOTES</span></span>

## <span data-ttu-id="755a4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="755a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="755a4-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="755a4-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="755a4-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="755a4-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


