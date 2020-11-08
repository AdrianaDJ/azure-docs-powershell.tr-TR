---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106145"
---
# <span data-ttu-id="828e0-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="828e0-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="828e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828e0-102">SYNOPSIS</span></span>
<span data-ttu-id="828e0-103">Ayrılmış IP adresini adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="828e0-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="828e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="828e0-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="828e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="828e0-105">DESCRIPTION</span></span>
<span data-ttu-id="828e0-106">**Remove-AzureReservedIP** cmdlet 'i ayrılmış bir IP adresini adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="828e0-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="828e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="828e0-107">EXAMPLES</span></span>

### <span data-ttu-id="828e0-108">Örnek 1: ayrılmış IP adresini adıyla kaldırma</span><span class="sxs-lookup"><span data-stu-id="828e0-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="828e0-109">Bu komut ayrılmış bir IP adresini adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="828e0-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="828e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="828e0-110">PARAMETERS</span></span>

### <span data-ttu-id="828e0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="828e0-111">-Force</span></span>
<span data-ttu-id="828e0-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="828e0-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828e0-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="828e0-113">-InformationAction</span></span>
<span data-ttu-id="828e0-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="828e0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="828e0-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="828e0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="828e0-116">'A</span><span class="sxs-lookup"><span data-stu-id="828e0-116">Continue</span></span>
- <span data-ttu-id="828e0-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="828e0-117">Ignore</span></span>
- <span data-ttu-id="828e0-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="828e0-118">Inquire</span></span>
- <span data-ttu-id="828e0-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="828e0-119">SilentlyContinue</span></span>
- <span data-ttu-id="828e0-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="828e0-120">Stop</span></span>
- <span data-ttu-id="828e0-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="828e0-121">Suspend</span></span>

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

### <span data-ttu-id="828e0-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="828e0-122">-InformationVariable</span></span>
<span data-ttu-id="828e0-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="828e0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="828e0-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="828e0-124">-Profile</span></span>
<span data-ttu-id="828e0-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="828e0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="828e0-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="828e0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="828e0-127">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="828e0-127">-ReservedIPName</span></span>
<span data-ttu-id="828e0-128">Ayrılmış IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="828e0-128">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828e0-129">CommonParameters</span></span>
<span data-ttu-id="828e0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="828e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828e0-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828e0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828e0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="828e0-132">INPUTS</span></span>

## <span data-ttu-id="828e0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="828e0-133">OUTPUTS</span></span>

## <span data-ttu-id="828e0-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="828e0-134">NOTES</span></span>

## <span data-ttu-id="828e0-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="828e0-135">RELATED LINKS</span></span>

[<span data-ttu-id="828e0-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="828e0-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="828e0-137">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="828e0-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="828e0-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="828e0-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


