---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106126"
---
# <span data-ttu-id="5e9ac-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5e9ac-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="5e9ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9ac-103">Belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti AD etki alanı uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5e9ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e9ac-104">SYNTAX</span></span>

### <span data-ttu-id="5e9ac-105">RemoveByRoles (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e9ac-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e9ac-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="5e9ac-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e9ac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e9ac-107">DESCRIPTION</span></span>
<span data-ttu-id="5e9ac-108">**Remove-AzureServiceADDomainExtension** cmdlet 'i, belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Active DIRECTORY (ad) etki alanı uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5e9ac-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e9ac-109">EXAMPLES</span></span>

### <span data-ttu-id="5e9ac-110">Örnek 1: AD etki alanı uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5e9ac-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="5e9ac-111">Bu komut $Svc değişkeniyle belirtilen uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="5e9ac-112">Örnek 2: belirtilen rolün AD etki alanı uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5e9ac-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="5e9ac-113">Bu komut belirtilen rolün hizmet uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="5e9ac-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e9ac-114">PARAMETERS</span></span>

### <span data-ttu-id="5e9ac-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5e9ac-115">-InformationAction</span></span>
<span data-ttu-id="5e9ac-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5e9ac-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5e9ac-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e9ac-118">'A</span><span class="sxs-lookup"><span data-stu-id="5e9ac-118">Continue</span></span>
- <span data-ttu-id="5e9ac-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="5e9ac-119">Ignore</span></span>
- <span data-ttu-id="5e9ac-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="5e9ac-120">Inquire</span></span>
- <span data-ttu-id="5e9ac-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="5e9ac-121">SilentlyContinue</span></span>
- <span data-ttu-id="5e9ac-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="5e9ac-122">Stop</span></span>
- <span data-ttu-id="5e9ac-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="5e9ac-123">Suspend</span></span>

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

### <span data-ttu-id="5e9ac-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="5e9ac-124">-InformationVariable</span></span>
<span data-ttu-id="5e9ac-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5e9ac-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="5e9ac-126">-Profile</span></span>
<span data-ttu-id="5e9ac-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e9ac-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e9ac-129">-Role</span><span class="sxs-lookup"><span data-stu-id="5e9ac-129">-Role</span></span>
<span data-ttu-id="5e9ac-130">Uzak Masaüstü yapılandırmasının belirtilmesi için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="5e9ac-131">Belirtilmemişse, AD etki alanı yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ac-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="5e9ac-132">-ServiceName</span></span>
<span data-ttu-id="5e9ac-133">Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-133">Specifies the name of an Azure service.</span></span>

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

### <span data-ttu-id="5e9ac-134">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="5e9ac-134">-Slot</span></span>
<span data-ttu-id="5e9ac-135">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="5e9ac-136">Geçerli değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="5e9ac-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e9ac-137">-UninstallConfiguration</span></span>
<span data-ttu-id="5e9ac-138">Bu cmdlet 'in bulut hizmetindeki tüm AD etki alanı yapılandırmalarını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e9ac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9ac-139">CommonParameters</span></span>
<span data-ttu-id="5e9ac-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e9ac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9ac-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e9ac-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9ac-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e9ac-142">INPUTS</span></span>

## <span data-ttu-id="5e9ac-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e9ac-143">OUTPUTS</span></span>

## <span data-ttu-id="5e9ac-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e9ac-144">NOTES</span></span>

## <span data-ttu-id="5e9ac-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e9ac-145">RELATED LINKS</span></span>

[<span data-ttu-id="5e9ac-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5e9ac-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="5e9ac-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5e9ac-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


