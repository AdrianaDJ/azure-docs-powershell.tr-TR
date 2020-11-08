---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105531"
---
# <span data-ttu-id="b4fa5-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4fa5-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="b4fa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fa5-103">Azure sanal makinesi özel komut dosyası uzantısından bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="b4fa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4fa5-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4fa5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fa5-106">**Get-AzureVMCustomScriptExtension** cmdlet 'ı bir Azure sanal makinesi özel komut dosyası uzantısından bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="b4fa5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4fa5-107">EXAMPLES</span></span>

### <span data-ttu-id="b4fa5-108">Örnek 1: Azure sanal makine Betik uzantısı alma</span><span class="sxs-lookup"><span data-stu-id="b4fa5-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="b4fa5-109">Bu komut, $VM değişkeninde depolanan bir Azure sanal makine komut dosyası uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="b4fa5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4fa5-110">PARAMETERS</span></span>

### <span data-ttu-id="b4fa5-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b4fa5-111">-InformationAction</span></span>
<span data-ttu-id="b4fa5-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4fa5-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b4fa5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4fa5-114">'A</span><span class="sxs-lookup"><span data-stu-id="b4fa5-114">Continue</span></span>
- <span data-ttu-id="b4fa5-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="b4fa5-115">Ignore</span></span>
- <span data-ttu-id="b4fa5-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b4fa5-116">Inquire</span></span>
- <span data-ttu-id="b4fa5-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b4fa5-117">SilentlyContinue</span></span>
- <span data-ttu-id="b4fa5-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b4fa5-118">Stop</span></span>
- <span data-ttu-id="b4fa5-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b4fa5-119">Suspend</span></span>

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

### <span data-ttu-id="b4fa5-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b4fa5-120">-InformationVariable</span></span>
<span data-ttu-id="b4fa5-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4fa5-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4fa5-122">-Profile</span></span>
<span data-ttu-id="b4fa5-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4fa5-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4fa5-125">-VM</span><span class="sxs-lookup"><span data-stu-id="b4fa5-125">-VM</span></span>
<span data-ttu-id="b4fa5-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b4fa5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fa5-127">CommonParameters</span></span>
<span data-ttu-id="b4fa5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4fa5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fa5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4fa5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fa5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4fa5-130">INPUTS</span></span>

## <span data-ttu-id="b4fa5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4fa5-131">OUTPUTS</span></span>

## <span data-ttu-id="b4fa5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4fa5-132">NOTES</span></span>

## <span data-ttu-id="b4fa5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4fa5-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4fa5-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4fa5-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="b4fa5-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4fa5-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


