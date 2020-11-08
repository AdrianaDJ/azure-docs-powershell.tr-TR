---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106244"
---
# <span data-ttu-id="8191e-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8191e-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="8191e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8191e-102">SYNOPSIS</span></span>
<span data-ttu-id="8191e-103">Üretim ve hazırlama arasındaki dağıtımları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8191e-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="8191e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8191e-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8191e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8191e-105">DESCRIPTION</span></span>
<span data-ttu-id="8191e-106">**Taþý-AzureDeployment** cmdlet 'i, üretim ve hazırlama ortamlarındaki dağıtımların sanal IP adreslerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8191e-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="8191e-107">Bu cmdlet, hazırlama ortamında çalışan bir dağıtımı üretim ortamına ve üretim ortamında hazırlama ortamına çalışan bir dağıtıma değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8191e-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="8191e-108">Hazırlama ortamında bir dağıtım ve üretim ortamında dağıtım olmazsa cmdlet, dağıtımı üretime taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="8191e-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="8191e-109">Üretim ortamında bir dağıtım ve hazırlama ortamında dağıtım olmazsa, cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="8191e-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="8191e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8191e-110">EXAMPLES</span></span>

### <span data-ttu-id="8191e-111">Örnek 1: hizmet için dağıtımları değiştirme</span><span class="sxs-lookup"><span data-stu-id="8191e-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="8191e-112">Bu komut, üretim ve hazırlama ortamları arasındaki ContosoService adındaki hizmetin dağıtımlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8191e-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="8191e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8191e-113">PARAMETERS</span></span>

### <span data-ttu-id="8191e-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8191e-114">-InformationAction</span></span>
<span data-ttu-id="8191e-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8191e-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8191e-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8191e-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8191e-117">'A</span><span class="sxs-lookup"><span data-stu-id="8191e-117">Continue</span></span>
- <span data-ttu-id="8191e-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="8191e-118">Ignore</span></span>
- <span data-ttu-id="8191e-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="8191e-119">Inquire</span></span>
- <span data-ttu-id="8191e-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="8191e-120">SilentlyContinue</span></span>
- <span data-ttu-id="8191e-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="8191e-121">Stop</span></span>
- <span data-ttu-id="8191e-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="8191e-122">Suspend</span></span>

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

### <span data-ttu-id="8191e-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="8191e-123">-InformationVariable</span></span>
<span data-ttu-id="8191e-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="8191e-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8191e-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="8191e-125">-Profile</span></span>
<span data-ttu-id="8191e-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8191e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8191e-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8191e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8191e-128">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="8191e-128">-ServiceName</span></span>
<span data-ttu-id="8191e-129">Bu cmdlet 'in üretimi ve hazırlama dağıtımlarını yerine çevireceğiniz hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8191e-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="8191e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8191e-130">CommonParameters</span></span>
<span data-ttu-id="8191e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8191e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8191e-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8191e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8191e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8191e-133">INPUTS</span></span>

## <span data-ttu-id="8191e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8191e-134">OUTPUTS</span></span>

### <span data-ttu-id="8191e-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8191e-135">ManagementOperationContext</span></span>

## <span data-ttu-id="8191e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8191e-136">NOTES</span></span>

## <span data-ttu-id="8191e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8191e-137">RELATED LINKS</span></span>

[<span data-ttu-id="8191e-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8191e-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="8191e-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="8191e-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="8191e-140">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8191e-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="8191e-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8191e-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="8191e-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8191e-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


