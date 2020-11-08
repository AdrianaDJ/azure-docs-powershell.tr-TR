---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105603"
---
# <span data-ttu-id="9312e-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9312e-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="9312e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9312e-102">SYNOPSIS</span></span>
<span data-ttu-id="9312e-103">Belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="9312e-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="9312e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9312e-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9312e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9312e-105">DESCRIPTION</span></span>
<span data-ttu-id="9312e-106">**Get-Azurezervicediagnoksextensextencmdlet** 'i, belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="9312e-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="9312e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9312e-107">EXAMPLES</span></span>

### <span data-ttu-id="9312e-108">Örnek 1: hizmet tanılama uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="9312e-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="9312e-109">Bu komut, tüm roller genelinde bir hizmetin hizmet tanılamayı alır.</span><span class="sxs-lookup"><span data-stu-id="9312e-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="9312e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9312e-110">PARAMETERS</span></span>

### <span data-ttu-id="9312e-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9312e-111">-InformationAction</span></span>
<span data-ttu-id="9312e-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9312e-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9312e-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9312e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9312e-114">'A</span><span class="sxs-lookup"><span data-stu-id="9312e-114">Continue</span></span>
- <span data-ttu-id="9312e-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="9312e-115">Ignore</span></span>
- <span data-ttu-id="9312e-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9312e-116">Inquire</span></span>
- <span data-ttu-id="9312e-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9312e-117">SilentlyContinue</span></span>
- <span data-ttu-id="9312e-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9312e-118">Stop</span></span>
- <span data-ttu-id="9312e-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9312e-119">Suspend</span></span>

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

### <span data-ttu-id="9312e-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9312e-120">-InformationVariable</span></span>
<span data-ttu-id="9312e-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9312e-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9312e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="9312e-122">-Profile</span></span>
<span data-ttu-id="9312e-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9312e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9312e-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9312e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9312e-125">-Role</span><span class="sxs-lookup"><span data-stu-id="9312e-125">-Role</span></span>
<span data-ttu-id="9312e-126">Rol dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9312e-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9312e-127">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="9312e-127">-ServiceName</span></span>
<span data-ttu-id="9312e-128">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9312e-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="9312e-129">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="9312e-129">-Slot</span></span>
<span data-ttu-id="9312e-130">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9312e-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="9312e-131">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="9312e-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="9312e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9312e-132">CommonParameters</span></span>
<span data-ttu-id="9312e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9312e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9312e-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9312e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9312e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9312e-135">INPUTS</span></span>

## <span data-ttu-id="9312e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9312e-136">OUTPUTS</span></span>

## <span data-ttu-id="9312e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9312e-137">NOTES</span></span>

## <span data-ttu-id="9312e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9312e-138">RELATED LINKS</span></span>

[<span data-ttu-id="9312e-139">Remove-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="9312e-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="9312e-140">Set-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="9312e-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


