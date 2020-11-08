---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106443"
---
# <span data-ttu-id="80c00-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="80c00-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="80c00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c00-102">SYNOPSIS</span></span>
<span data-ttu-id="80c00-103">Sanal makineye uygulanan Pupalı uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80c00-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="80c00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80c00-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80c00-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80c00-105">DESCRIPTION</span></span>
<span data-ttu-id="80c00-106">**Remove-AzureVMPuppetExtension** cmdlet 'i, sanal makineye uygulanan Pupevcil hayvan uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80c00-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="80c00-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80c00-107">EXAMPLES</span></span>

### <span data-ttu-id="80c00-108">Örnek 1: sanal makineye uygulanan Pupalı uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="80c00-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="80c00-109">Bu komut belirtilen sanal makineye uygulanan Pupevcil hayvan uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="80c00-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="80c00-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80c00-110">PARAMETERS</span></span>

### <span data-ttu-id="80c00-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="80c00-111">-InformationAction</span></span>
<span data-ttu-id="80c00-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="80c00-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80c00-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="80c00-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80c00-114">'A</span><span class="sxs-lookup"><span data-stu-id="80c00-114">Continue</span></span>
- <span data-ttu-id="80c00-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="80c00-115">Ignore</span></span>
- <span data-ttu-id="80c00-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="80c00-116">Inquire</span></span>
- <span data-ttu-id="80c00-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="80c00-117">SilentlyContinue</span></span>
- <span data-ttu-id="80c00-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="80c00-118">Stop</span></span>
- <span data-ttu-id="80c00-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="80c00-119">Suspend</span></span>

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

### <span data-ttu-id="80c00-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="80c00-120">-InformationVariable</span></span>
<span data-ttu-id="80c00-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="80c00-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="80c00-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="80c00-122">-Profile</span></span>
<span data-ttu-id="80c00-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="80c00-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80c00-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="80c00-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80c00-125">-VM</span><span class="sxs-lookup"><span data-stu-id="80c00-125">-VM</span></span>
<span data-ttu-id="80c00-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="80c00-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="80c00-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c00-127">CommonParameters</span></span>
<span data-ttu-id="80c00-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80c00-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c00-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c00-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c00-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80c00-130">INPUTS</span></span>

## <span data-ttu-id="80c00-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80c00-131">OUTPUTS</span></span>

## <span data-ttu-id="80c00-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80c00-132">NOTES</span></span>

## <span data-ttu-id="80c00-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80c00-133">RELATED LINKS</span></span>

[<span data-ttu-id="80c00-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="80c00-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="80c00-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="80c00-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


