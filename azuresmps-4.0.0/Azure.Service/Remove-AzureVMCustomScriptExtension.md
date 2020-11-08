---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106448"
---
# <span data-ttu-id="ff07b-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ff07b-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="ff07b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff07b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff07b-103">Sanal makineden özel komut dosyası uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff07b-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="ff07b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff07b-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff07b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff07b-105">DESCRIPTION</span></span>
<span data-ttu-id="ff07b-106">**Remove-AzureVMCustomScriptExtension** cmdlet 'i, bir sanal makineden özel betik uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff07b-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="ff07b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff07b-107">EXAMPLES</span></span>

### <span data-ttu-id="ff07b-108">Örnek 1: sanal makine özel betik uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ff07b-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="ff07b-109">Bu komut, belirtilen sanal makineden Azure sanal makine özel komut dosyası uzantısını değişken $VM depolandığından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff07b-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="ff07b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff07b-110">PARAMETERS</span></span>

### <span data-ttu-id="ff07b-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ff07b-111">-InformationAction</span></span>
<span data-ttu-id="ff07b-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff07b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff07b-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ff07b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff07b-114">'A</span><span class="sxs-lookup"><span data-stu-id="ff07b-114">Continue</span></span>
- <span data-ttu-id="ff07b-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="ff07b-115">Ignore</span></span>
- <span data-ttu-id="ff07b-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ff07b-116">Inquire</span></span>
- <span data-ttu-id="ff07b-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ff07b-117">SilentlyContinue</span></span>
- <span data-ttu-id="ff07b-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ff07b-118">Stop</span></span>
- <span data-ttu-id="ff07b-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ff07b-119">Suspend</span></span>

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

### <span data-ttu-id="ff07b-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ff07b-120">-InformationVariable</span></span>
<span data-ttu-id="ff07b-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff07b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff07b-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff07b-122">-Profile</span></span>
<span data-ttu-id="ff07b-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff07b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff07b-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ff07b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff07b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="ff07b-125">-VM</span></span>
<span data-ttu-id="ff07b-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff07b-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ff07b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff07b-127">CommonParameters</span></span>
<span data-ttu-id="ff07b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff07b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff07b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff07b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff07b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff07b-130">INPUTS</span></span>

## <span data-ttu-id="ff07b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff07b-131">OUTPUTS</span></span>

## <span data-ttu-id="ff07b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff07b-132">NOTES</span></span>

## <span data-ttu-id="ff07b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff07b-133">RELATED LINKS</span></span>

[<span data-ttu-id="ff07b-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ff07b-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="ff07b-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ff07b-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


