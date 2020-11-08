---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105535"
---
# <span data-ttu-id="2cfc8-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2cfc8-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="2cfc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cfc8-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfc8-103">Sanal makineye uygulanan VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2cfc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cfc8-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2cfc8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cfc8-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfc8-106">**Get-AzureVMAccessExtension** cmdlet 'i sanal makineye uygulanan VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="2cfc8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cfc8-107">EXAMPLES</span></span>

### <span data-ttu-id="2cfc8-108">Örnek 1: sanal makinenin VMAccess uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="2cfc8-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="2cfc8-109">Bu komut, bir sanal makinenin VMAccess uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="2cfc8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cfc8-110">PARAMETERS</span></span>

### <span data-ttu-id="2cfc8-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2cfc8-111">-InformationAction</span></span>
<span data-ttu-id="2cfc8-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2cfc8-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2cfc8-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfc8-114">'A</span><span class="sxs-lookup"><span data-stu-id="2cfc8-114">Continue</span></span>
- <span data-ttu-id="2cfc8-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="2cfc8-115">Ignore</span></span>
- <span data-ttu-id="2cfc8-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2cfc8-116">Inquire</span></span>
- <span data-ttu-id="2cfc8-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2cfc8-117">SilentlyContinue</span></span>
- <span data-ttu-id="2cfc8-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2cfc8-118">Stop</span></span>
- <span data-ttu-id="2cfc8-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2cfc8-119">Suspend</span></span>

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

### <span data-ttu-id="2cfc8-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2cfc8-120">-InformationVariable</span></span>
<span data-ttu-id="2cfc8-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2cfc8-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2cfc8-122">-Profile</span></span>
<span data-ttu-id="2cfc8-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2cfc8-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2cfc8-125">-VM</span><span class="sxs-lookup"><span data-stu-id="2cfc8-125">-VM</span></span>
<span data-ttu-id="2cfc8-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2cfc8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfc8-127">CommonParameters</span></span>
<span data-ttu-id="2cfc8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfc8-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cfc8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfc8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cfc8-130">INPUTS</span></span>

## <span data-ttu-id="2cfc8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cfc8-131">OUTPUTS</span></span>

## <span data-ttu-id="2cfc8-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cfc8-132">NOTES</span></span>

## <span data-ttu-id="2cfc8-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cfc8-133">RELATED LINKS</span></span>

[<span data-ttu-id="2cfc8-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2cfc8-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="2cfc8-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2cfc8-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


