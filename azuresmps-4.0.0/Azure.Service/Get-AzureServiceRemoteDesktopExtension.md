---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105596"
---
# <span data-ttu-id="85353-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="85353-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="85353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85353-102">SYNOPSIS</span></span>
<span data-ttu-id="85353-103">Bu cmdlet, belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Uzak Masaüstü uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="85353-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="85353-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85353-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="85353-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85353-105">DESCRIPTION</span></span>
<span data-ttu-id="85353-106">**Get-Azurezerviceremotedesktopextension** cmdlet 'i, belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti uzak masaüstü uzantısı 'nı alır.</span><span class="sxs-lookup"><span data-stu-id="85353-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="85353-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85353-107">EXAMPLES</span></span>

### <span data-ttu-id="85353-108">Örnek 1: belirtilen hizmet için Uzak Masaüstü uzantısı</span><span class="sxs-lookup"><span data-stu-id="85353-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="85353-109">Bu komut, belirtilen hizmetin Uzak Masaüstü uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="85353-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="85353-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85353-110">PARAMETERS</span></span>

### <span data-ttu-id="85353-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="85353-111">-InformationAction</span></span>
<span data-ttu-id="85353-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85353-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="85353-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="85353-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85353-114">'A</span><span class="sxs-lookup"><span data-stu-id="85353-114">Continue</span></span>
- <span data-ttu-id="85353-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="85353-115">Ignore</span></span>
- <span data-ttu-id="85353-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="85353-116">Inquire</span></span>
- <span data-ttu-id="85353-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="85353-117">SilentlyContinue</span></span>
- <span data-ttu-id="85353-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="85353-118">Stop</span></span>
- <span data-ttu-id="85353-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="85353-119">Suspend</span></span>

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

### <span data-ttu-id="85353-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="85353-120">-InformationVariable</span></span>
<span data-ttu-id="85353-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="85353-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="85353-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="85353-122">-Profile</span></span>
<span data-ttu-id="85353-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85353-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85353-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="85353-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85353-125">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="85353-125">-ServiceName</span></span>
<span data-ttu-id="85353-126">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85353-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85353-127">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="85353-127">-Slot</span></span>
<span data-ttu-id="85353-128">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85353-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="85353-129">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="85353-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85353-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85353-130">CommonParameters</span></span>
<span data-ttu-id="85353-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85353-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85353-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85353-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85353-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85353-133">INPUTS</span></span>

## <span data-ttu-id="85353-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85353-134">OUTPUTS</span></span>

## <span data-ttu-id="85353-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85353-135">NOTES</span></span>

## <span data-ttu-id="85353-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85353-136">RELATED LINKS</span></span>

[<span data-ttu-id="85353-137">Set-Azurezerviceremotedesktopextension</span><span class="sxs-lookup"><span data-stu-id="85353-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


