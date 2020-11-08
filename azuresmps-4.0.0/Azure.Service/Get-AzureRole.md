---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106314"
---
# <span data-ttu-id="b55b3-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="b55b3-101">Get-AzureRole</span></span>

## <span data-ttu-id="b55b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b55b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b55b3-103">Microsoft Azure hizmetinizden rollerin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55b3-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="b55b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b55b3-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b55b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b55b3-105">DESCRIPTION</span></span>
<span data-ttu-id="b55b3-106">**Get-AzureRole** cmdlet 'ı, Microsoft Azure hizmetinizden rollerle ilgili ayrıntılar içeren bir liste nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55b3-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="b55b3-107">*RoleName* parametresini belirtirseniz **Get-AzureRole** yalnızca bu rolle ilgili ayrıntıları döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55b3-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="b55b3-108">*Instancedetails* parametresini belirtirseniz, örneğe özgü ek ayrıntılar verilir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="b55b3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b55b3-109">EXAMPLES</span></span>

### <span data-ttu-id="b55b3-110">Örnek 1: hizmet rollerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="b55b3-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="b55b3-111">Bu komut, MySvc01 hizmetinde çalışan tüm üretim rollerinde ayrıntılı bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55b3-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="b55b3-112">Örnek 2: hizmette çalışan bir role ilişkin ayrıntıları alma</span><span class="sxs-lookup"><span data-stu-id="b55b3-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="b55b3-113">Bu komut, MySvc01 hizmetinin hazırlama ortamında çalışan MyTestVM3 rolündeki ayrıntılar içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55b3-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="b55b3-114">Örnek 3: hizmette çalışan bir rolün örneklerine örnek bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="b55b3-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="b55b3-115">Bu komut, MySvc01 hizmetindeki üretim ortamında çalışan MyTestVM02 rolünün örneklerinin ayrıntılarını içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b55b3-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="b55b3-116">Örnek 4: hizmetle ilişkilendirilmiş rol örneklerinin tablosunu alma</span><span class="sxs-lookup"><span data-stu-id="b55b3-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="b55b3-117">Bu komut, MySvc01 hizmetindeki üretim ortamında çalışan tüm rol örneklerinin örnek adına, boyutuna ve durumuna döner.</span><span class="sxs-lookup"><span data-stu-id="b55b3-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="b55b3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b55b3-118">PARAMETERS</span></span>

### <span data-ttu-id="b55b3-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b55b3-119">-InformationAction</span></span>
<span data-ttu-id="b55b3-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b55b3-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b55b3-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b55b3-122">'A</span><span class="sxs-lookup"><span data-stu-id="b55b3-122">Continue</span></span>
- <span data-ttu-id="b55b3-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="b55b3-123">Ignore</span></span>
- <span data-ttu-id="b55b3-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b55b3-124">Inquire</span></span>
- <span data-ttu-id="b55b3-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b55b3-125">SilentlyContinue</span></span>
- <span data-ttu-id="b55b3-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b55b3-126">Stop</span></span>
- <span data-ttu-id="b55b3-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b55b3-127">Suspend</span></span>

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

### <span data-ttu-id="b55b3-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b55b3-128">-InformationVariable</span></span>
<span data-ttu-id="b55b3-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b55b3-130">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="b55b3-130">-InstanceDetails</span></span>
<span data-ttu-id="b55b3-131">Bu cmdlet 'in her roldeki örneklerin ayrıntılarını döndürmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b55b3-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="b55b3-132">-Profile</span></span>
<span data-ttu-id="b55b3-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b55b3-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b55b3-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b55b3-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b55b3-135">-RoleName</span></span>
<span data-ttu-id="b55b3-136">Alınacak rolün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b55b3-137">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="b55b3-137">-ServiceName</span></span>
<span data-ttu-id="b55b3-138">Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="b55b3-139">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="b55b3-139">-Slot</span></span>
<span data-ttu-id="b55b3-140">Azure dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b55b3-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="b55b3-141">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="b55b3-141">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="b55b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55b3-142">CommonParameters</span></span>
<span data-ttu-id="b55b3-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b55b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55b3-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55b3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55b3-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b55b3-145">INPUTS</span></span>

## <span data-ttu-id="b55b3-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b55b3-146">OUTPUTS</span></span>

## <span data-ttu-id="b55b3-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b55b3-147">NOTES</span></span>

## <span data-ttu-id="b55b3-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b55b3-148">RELATED LINKS</span></span>

[<span data-ttu-id="b55b3-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="b55b3-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


