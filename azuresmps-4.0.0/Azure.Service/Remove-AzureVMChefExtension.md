---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105505"
---
# <span data-ttu-id="19c0e-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="19c0e-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="19c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="19c0e-103">Sanal makinede uygulanan Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19c0e-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="19c0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19c0e-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19c0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="19c0e-106">**Remove-AzureVMChefExtension** cmdlet 'i sanal makinede uygulanan Chef uzantısını siler.</span><span class="sxs-lookup"><span data-stu-id="19c0e-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="19c0e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="19c0e-108">Örnek 1: belirtilen sanal makineye uygulanan Chef uzantısını kaldırın</span><span class="sxs-lookup"><span data-stu-id="19c0e-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="19c0e-109">Bu komut sanal makinede uygulanan Chef uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19c0e-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="19c0e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19c0e-110">PARAMETERS</span></span>

### <span data-ttu-id="19c0e-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="19c0e-111">-InformationAction</span></span>
<span data-ttu-id="19c0e-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19c0e-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19c0e-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="19c0e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19c0e-114">'A</span><span class="sxs-lookup"><span data-stu-id="19c0e-114">Continue</span></span>
- <span data-ttu-id="19c0e-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="19c0e-115">Ignore</span></span>
- <span data-ttu-id="19c0e-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="19c0e-116">Inquire</span></span>
- <span data-ttu-id="19c0e-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="19c0e-117">SilentlyContinue</span></span>
- <span data-ttu-id="19c0e-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="19c0e-118">Stop</span></span>
- <span data-ttu-id="19c0e-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="19c0e-119">Suspend</span></span>

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

### <span data-ttu-id="19c0e-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="19c0e-120">-InformationVariable</span></span>
<span data-ttu-id="19c0e-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="19c0e-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="19c0e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="19c0e-122">-Profile</span></span>
<span data-ttu-id="19c0e-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19c0e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19c0e-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="19c0e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19c0e-125">-VM</span><span class="sxs-lookup"><span data-stu-id="19c0e-125">-VM</span></span>
<span data-ttu-id="19c0e-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19c0e-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="19c0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c0e-127">CommonParameters</span></span>
<span data-ttu-id="19c0e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19c0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c0e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c0e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c0e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19c0e-130">INPUTS</span></span>

## <span data-ttu-id="19c0e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19c0e-131">OUTPUTS</span></span>

## <span data-ttu-id="19c0e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19c0e-132">NOTES</span></span>

## <span data-ttu-id="19c0e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19c0e-133">RELATED LINKS</span></span>

[<span data-ttu-id="19c0e-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="19c0e-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="19c0e-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="19c0e-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


