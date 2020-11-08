---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106355"
---
# <span data-ttu-id="cf2c2-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="cf2c2-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="cf2c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2c2-103">Dağıtımın ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="cf2c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf2c2-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cf2c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2c2-106">**Get-AzureDeployment** cmdlet 'ı bir Azure dağıtımının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="cf2c2-107">Azure hizmetinin adını ve dağıtımın yuvasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="cf2c2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf2c2-108">EXAMPLES</span></span>

### <span data-ttu-id="cf2c2-109">Örnek 1: bir üretim dağıtımının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="cf2c2-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="cf2c2-110">Bu komut, ContosoService adlı hizmetin dağıtımının ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="cf2c2-111">Bu komut bir yuva belirtmez.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-111">This command does not specify a slot.</span></span>
<span data-ttu-id="cf2c2-112">Bu nedenle, komut üretim varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="cf2c2-113">Örnek 2: düzeylendirme dağıtımının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="cf2c2-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="cf2c2-114">Bu komut, Contosohizmetinin hazırlama dağıtımının ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="cf2c2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf2c2-115">PARAMETERS</span></span>

### <span data-ttu-id="cf2c2-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cf2c2-116">-InformationAction</span></span>
<span data-ttu-id="cf2c2-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cf2c2-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cf2c2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf2c2-119">'A</span><span class="sxs-lookup"><span data-stu-id="cf2c2-119">Continue</span></span>
- <span data-ttu-id="cf2c2-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="cf2c2-120">Ignore</span></span>
- <span data-ttu-id="cf2c2-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="cf2c2-121">Inquire</span></span>
- <span data-ttu-id="cf2c2-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="cf2c2-122">SilentlyContinue</span></span>
- <span data-ttu-id="cf2c2-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cf2c2-123">Stop</span></span>
- <span data-ttu-id="cf2c2-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="cf2c2-124">Suspend</span></span>

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

### <span data-ttu-id="cf2c2-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="cf2c2-125">-InformationVariable</span></span>
<span data-ttu-id="cf2c2-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cf2c2-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="cf2c2-127">-Profile</span></span>
<span data-ttu-id="cf2c2-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf2c2-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf2c2-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="cf2c2-130">-ServiceName</span></span>
<span data-ttu-id="cf2c2-131">Hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="cf2c2-132">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="cf2c2-132">-Slot</span></span>
<span data-ttu-id="cf2c2-133">Dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="cf2c2-134">Geçerli değerler: hazırlama veya üretim.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="cf2c2-135">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2c2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2c2-136">CommonParameters</span></span>
<span data-ttu-id="cf2c2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2c2-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2c2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2c2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf2c2-139">INPUTS</span></span>

## <span data-ttu-id="cf2c2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf2c2-140">OUTPUTS</span></span>

## <span data-ttu-id="cf2c2-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf2c2-141">NOTES</span></span>

## <span data-ttu-id="cf2c2-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf2c2-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf2c2-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="cf2c2-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="cf2c2-144">Taşı-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="cf2c2-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="cf2c2-145">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="cf2c2-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="cf2c2-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="cf2c2-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="cf2c2-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="cf2c2-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


