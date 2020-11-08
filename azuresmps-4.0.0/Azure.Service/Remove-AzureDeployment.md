---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106165"
---
# <span data-ttu-id="3058d-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3058d-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="3058d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3058d-102">SYNOPSIS</span></span>
<span data-ttu-id="3058d-103">Bulut hizmetinin dağıtımını siler.</span><span class="sxs-lookup"><span data-stu-id="3058d-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="3058d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3058d-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3058d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3058d-105">DESCRIPTION</span></span>
<span data-ttu-id="3058d-106">**Remove-AzureDeployment** cmdlet 'ı bir Azure bulut hizmetinin dağıtımını siler.</span><span class="sxs-lookup"><span data-stu-id="3058d-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="3058d-107">Bir dağıtımı silmek için önce askıya alın.</span><span class="sxs-lookup"><span data-stu-id="3058d-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="3058d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3058d-108">EXAMPLES</span></span>

### <span data-ttu-id="3058d-109">Örnek 1: dağıtımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="3058d-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="3058d-110">Bu komut, ContosoService adlı Azure hizmetinin dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3058d-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="3058d-111">Bu komut bir yuva belirtmediğinden, hizmeti üretim ortamından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3058d-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="3058d-112">Örnek 2: dağıtım ve sanal sabit diskleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="3058d-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="3058d-113">Bu komut, ContosoService adlı hizmetin üretim ortamından dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3058d-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="3058d-114">Komut ayrıca temel sanal sabit diskleri de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3058d-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="3058d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3058d-115">PARAMETERS</span></span>

### <span data-ttu-id="3058d-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="3058d-116">-DeleteVHD</span></span>
<span data-ttu-id="3058d-117">Bu cmdlet 'in, blob depolamasındaki dağıtımı ve sanal sabit diskleri (VHD 'ler) kaldırdığından emin olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="3058d-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3058d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3058d-118">-Force</span></span>
<span data-ttu-id="3058d-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3058d-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3058d-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3058d-120">-InformationAction</span></span>
<span data-ttu-id="3058d-121">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3058d-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3058d-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3058d-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3058d-123">'A</span><span class="sxs-lookup"><span data-stu-id="3058d-123">Continue</span></span>
- <span data-ttu-id="3058d-124">Manıza</span><span class="sxs-lookup"><span data-stu-id="3058d-124">Ignore</span></span>
- <span data-ttu-id="3058d-125">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="3058d-125">Inquire</span></span>
- <span data-ttu-id="3058d-126">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="3058d-126">SilentlyContinue</span></span>
- <span data-ttu-id="3058d-127">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="3058d-127">Stop</span></span>
- <span data-ttu-id="3058d-128">Biliriz</span><span class="sxs-lookup"><span data-stu-id="3058d-128">Suspend</span></span>

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

### <span data-ttu-id="3058d-129">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="3058d-129">-InformationVariable</span></span>
<span data-ttu-id="3058d-130">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="3058d-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3058d-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="3058d-131">-Profile</span></span>
<span data-ttu-id="3058d-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3058d-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3058d-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3058d-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3058d-134">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="3058d-134">-ServiceName</span></span>
<span data-ttu-id="3058d-135">Bu cmdlet 'in bir dağıtımı sildiği hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3058d-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="3058d-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="3058d-136">-Slot</span></span>
<span data-ttu-id="3058d-137">Bu cmdlet 'in dağıtımı sildiği dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3058d-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="3058d-138">Geçerli değerler: hazırlama ve üretim.</span><span class="sxs-lookup"><span data-stu-id="3058d-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="3058d-139">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="3058d-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3058d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3058d-140">CommonParameters</span></span>
<span data-ttu-id="3058d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3058d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3058d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3058d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3058d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3058d-143">INPUTS</span></span>

## <span data-ttu-id="3058d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3058d-144">OUTPUTS</span></span>

### <span data-ttu-id="3058d-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="3058d-145">ManagementOperationContext</span></span>

## <span data-ttu-id="3058d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3058d-146">NOTES</span></span>

## <span data-ttu-id="3058d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3058d-147">RELATED LINKS</span></span>

[<span data-ttu-id="3058d-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3058d-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="3058d-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="3058d-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="3058d-150">Taşı-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3058d-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="3058d-151">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3058d-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="3058d-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3058d-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


