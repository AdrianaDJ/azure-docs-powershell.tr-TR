---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106545"
---
# <span data-ttu-id="abf47-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="abf47-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="abf47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf47-102">SYNOPSIS</span></span>
<span data-ttu-id="abf47-103">Sanal makineye uygulanan Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="abf47-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="abf47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abf47-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="abf47-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="abf47-105">DESCRIPTION</span></span>
<span data-ttu-id="abf47-106">**Get-AzureVMChefExtension** cmdlet 'i sanal makineye uygulanan Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="abf47-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="abf47-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abf47-107">EXAMPLES</span></span>

### <span data-ttu-id="abf47-108">Örnek 1: belirtilen sanal makineye, Chef uzantısının uygulanmasını sağlayın</span><span class="sxs-lookup"><span data-stu-id="abf47-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="abf47-109">Bu komut belirtilen sanal makineye uygulanan Chef uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="abf47-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="abf47-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abf47-110">PARAMETERS</span></span>

### <span data-ttu-id="abf47-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="abf47-111">-InformationAction</span></span>
<span data-ttu-id="abf47-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf47-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="abf47-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="abf47-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="abf47-114">'A</span><span class="sxs-lookup"><span data-stu-id="abf47-114">Continue</span></span>
- <span data-ttu-id="abf47-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="abf47-115">Ignore</span></span>
- <span data-ttu-id="abf47-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="abf47-116">Inquire</span></span>
- <span data-ttu-id="abf47-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="abf47-117">SilentlyContinue</span></span>
- <span data-ttu-id="abf47-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="abf47-118">Stop</span></span>
- <span data-ttu-id="abf47-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="abf47-119">Suspend</span></span>

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

### <span data-ttu-id="abf47-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="abf47-120">-InformationVariable</span></span>
<span data-ttu-id="abf47-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf47-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="abf47-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="abf47-122">-Profile</span></span>
<span data-ttu-id="abf47-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf47-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="abf47-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="abf47-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="abf47-125">-VM</span><span class="sxs-lookup"><span data-stu-id="abf47-125">-VM</span></span>
<span data-ttu-id="abf47-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abf47-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="abf47-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf47-127">CommonParameters</span></span>
<span data-ttu-id="abf47-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abf47-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf47-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf47-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf47-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abf47-130">INPUTS</span></span>

## <span data-ttu-id="abf47-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abf47-131">OUTPUTS</span></span>

## <span data-ttu-id="abf47-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abf47-132">NOTES</span></span>

## <span data-ttu-id="abf47-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abf47-133">RELATED LINKS</span></span>

[<span data-ttu-id="abf47-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="abf47-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="abf47-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="abf47-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


