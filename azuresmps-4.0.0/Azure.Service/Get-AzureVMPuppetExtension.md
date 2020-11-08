---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106526"
---
# <span data-ttu-id="fff19-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fff19-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="fff19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff19-102">SYNOPSIS</span></span>
<span data-ttu-id="fff19-103">Sanal makinede Pupevcil hayvan uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="fff19-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fff19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fff19-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fff19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fff19-105">DESCRIPTION</span></span>
<span data-ttu-id="fff19-106">**Get-AzureVMPuppetExtension** cmdlet 'i sanal makineye uygulanan Pupevcil hayvan uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="fff19-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fff19-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fff19-107">EXAMPLES</span></span>

### <span data-ttu-id="fff19-108">Örnek 1: sanal makineye Pupalı uzantısının uygulanmasını sağlayın</span><span class="sxs-lookup"><span data-stu-id="fff19-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="fff19-109">Bu komut, sanal makineye uygulanan Pupevcil hayvan uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="fff19-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fff19-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fff19-110">PARAMETERS</span></span>

### <span data-ttu-id="fff19-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fff19-111">-InformationAction</span></span>
<span data-ttu-id="fff19-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fff19-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fff19-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fff19-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fff19-114">'A</span><span class="sxs-lookup"><span data-stu-id="fff19-114">Continue</span></span>
- <span data-ttu-id="fff19-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="fff19-115">Ignore</span></span>
- <span data-ttu-id="fff19-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fff19-116">Inquire</span></span>
- <span data-ttu-id="fff19-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fff19-117">SilentlyContinue</span></span>
- <span data-ttu-id="fff19-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fff19-118">Stop</span></span>
- <span data-ttu-id="fff19-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fff19-119">Suspend</span></span>

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

### <span data-ttu-id="fff19-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fff19-120">-InformationVariable</span></span>
<span data-ttu-id="fff19-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fff19-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fff19-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="fff19-122">-Profile</span></span>
<span data-ttu-id="fff19-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fff19-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fff19-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fff19-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fff19-125">-VM</span><span class="sxs-lookup"><span data-stu-id="fff19-125">-VM</span></span>
<span data-ttu-id="fff19-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fff19-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fff19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff19-127">CommonParameters</span></span>
<span data-ttu-id="fff19-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fff19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff19-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fff19-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff19-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fff19-130">INPUTS</span></span>

## <span data-ttu-id="fff19-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fff19-131">OUTPUTS</span></span>

## <span data-ttu-id="fff19-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fff19-132">NOTES</span></span>

## <span data-ttu-id="fff19-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fff19-133">RELATED LINKS</span></span>

[<span data-ttu-id="fff19-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fff19-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="fff19-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="fff19-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


