---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105805"
---
# <span data-ttu-id="f6fda-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="f6fda-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="f6fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6fda-102">SYNOPSIS</span></span>

## <span data-ttu-id="f6fda-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6fda-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f6fda-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6fda-104">DESCRIPTION</span></span>

## <span data-ttu-id="f6fda-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6fda-105">EXAMPLES</span></span>

### <span data-ttu-id="f6fda-106">2</span><span class="sxs-lookup"><span data-stu-id="f6fda-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f6fda-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6fda-107">PARAMETERS</span></span>

### <span data-ttu-id="f6fda-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f6fda-108">-InformationAction</span></span>
<span data-ttu-id="f6fda-109">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6fda-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f6fda-110">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f6fda-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6fda-111">'A</span><span class="sxs-lookup"><span data-stu-id="f6fda-111">Continue</span></span>
- <span data-ttu-id="f6fda-112">Manıza</span><span class="sxs-lookup"><span data-stu-id="f6fda-112">Ignore</span></span>
- <span data-ttu-id="f6fda-113">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f6fda-113">Inquire</span></span>
- <span data-ttu-id="f6fda-114">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f6fda-114">SilentlyContinue</span></span>
- <span data-ttu-id="f6fda-115">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f6fda-115">Stop</span></span>
- <span data-ttu-id="f6fda-116">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f6fda-116">Suspend</span></span>

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

### <span data-ttu-id="f6fda-117">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f6fda-117">-InformationVariable</span></span>
<span data-ttu-id="f6fda-118">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6fda-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f6fda-119">-Ipiletme</span><span class="sxs-lookup"><span data-stu-id="f6fda-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fda-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6fda-120">-Name</span></span>
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

### <span data-ttu-id="f6fda-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f6fda-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fda-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6fda-122">-Profile</span></span>
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

### <span data-ttu-id="f6fda-123">-Staticvnetıpaddress</span><span class="sxs-lookup"><span data-stu-id="f6fda-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fda-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f6fda-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fda-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f6fda-125">-VM</span></span>
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

### <span data-ttu-id="f6fda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fda-126">CommonParameters</span></span>
<span data-ttu-id="f6fda-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6fda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fda-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fda-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fda-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6fda-129">INPUTS</span></span>

## <span data-ttu-id="f6fda-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6fda-130">OUTPUTS</span></span>

## <span data-ttu-id="f6fda-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6fda-131">NOTES</span></span>

## <span data-ttu-id="f6fda-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6fda-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6fda-133">Add-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="f6fda-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="f6fda-134">Get-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="f6fda-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="f6fda-135">Remove-Azurenetworkınterfaceconfig</span><span class="sxs-lookup"><span data-stu-id="f6fda-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


