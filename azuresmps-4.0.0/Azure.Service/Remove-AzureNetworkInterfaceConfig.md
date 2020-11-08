---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106466"
---
# <span data-ttu-id="c5c27-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="c5c27-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="c5c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c27-102">SYNOPSIS</span></span>

## <span data-ttu-id="c5c27-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5c27-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c5c27-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5c27-104">DESCRIPTION</span></span>

## <span data-ttu-id="c5c27-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5c27-105">EXAMPLES</span></span>

### <span data-ttu-id="c5c27-106">2</span><span class="sxs-lookup"><span data-stu-id="c5c27-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c5c27-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5c27-107">PARAMETERS</span></span>

### <span data-ttu-id="c5c27-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c5c27-108">-InformationAction</span></span>
<span data-ttu-id="c5c27-109">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5c27-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c5c27-110">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c5c27-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5c27-111">'A</span><span class="sxs-lookup"><span data-stu-id="c5c27-111">Continue</span></span>
- <span data-ttu-id="c5c27-112">Manıza</span><span class="sxs-lookup"><span data-stu-id="c5c27-112">Ignore</span></span>
- <span data-ttu-id="c5c27-113">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="c5c27-113">Inquire</span></span>
- <span data-ttu-id="c5c27-114">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="c5c27-114">SilentlyContinue</span></span>
- <span data-ttu-id="c5c27-115">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="c5c27-115">Stop</span></span>
- <span data-ttu-id="c5c27-116">Biliriz</span><span class="sxs-lookup"><span data-stu-id="c5c27-116">Suspend</span></span>

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

### <span data-ttu-id="c5c27-117">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="c5c27-117">-InformationVariable</span></span>
<span data-ttu-id="c5c27-118">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5c27-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c5c27-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5c27-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c27-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="c5c27-120">-Profile</span></span>
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

### <span data-ttu-id="c5c27-121">-VM</span><span class="sxs-lookup"><span data-stu-id="c5c27-121">-VM</span></span>
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

### <span data-ttu-id="c5c27-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c27-122">CommonParameters</span></span>
<span data-ttu-id="c5c27-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5c27-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c27-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c27-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c27-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5c27-125">INPUTS</span></span>

## <span data-ttu-id="c5c27-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5c27-126">OUTPUTS</span></span>

## <span data-ttu-id="c5c27-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5c27-127">NOTES</span></span>

## <span data-ttu-id="c5c27-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5c27-128">RELATED LINKS</span></span>

[<span data-ttu-id="c5c27-129">Add-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="c5c27-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="c5c27-130">Get-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="c5c27-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="c5c27-131">Set-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="c5c27-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


