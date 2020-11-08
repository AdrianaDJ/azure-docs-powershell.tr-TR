---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106113"
---
# <span data-ttu-id="eee50-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="eee50-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="eee50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee50-102">SYNOPSIS</span></span>
<span data-ttu-id="eee50-103">Dağıtıma uygulanan bulut hizmeti uzantılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eee50-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="eee50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eee50-104">SYNTAX</span></span>

### <span data-ttu-id="eee50-105">RemoveByRoles (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eee50-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eee50-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="eee50-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eee50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eee50-107">DESCRIPTION</span></span>
<span data-ttu-id="eee50-108">**Remove-AzureServiceExtension** cmdlet 'i, dağıtıma uygulanan bulut hizmeti uzantılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eee50-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="eee50-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eee50-109">EXAMPLES</span></span>

### <span data-ttu-id="eee50-110">Örnek 1: hizmet uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="eee50-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="eee50-111">Bu komut, hizmet uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eee50-111">This command removes a service extension.</span></span>

### <span data-ttu-id="eee50-112">Örnek 2: hizmet uzantısını kaldırma ve tüm yapılandırmaları kaldırma</span><span class="sxs-lookup"><span data-stu-id="eee50-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="eee50-113">Bu komut, hizmet uzantısını kaldırır ve tüm yapılandırmaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eee50-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="eee50-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eee50-114">PARAMETERS</span></span>

### <span data-ttu-id="eee50-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="eee50-115">-ExtensionName</span></span>
<span data-ttu-id="eee50-116">Uzantı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee50-117">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="eee50-117">-InformationAction</span></span>
<span data-ttu-id="eee50-118">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eee50-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eee50-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eee50-120">'A</span><span class="sxs-lookup"><span data-stu-id="eee50-120">Continue</span></span>
- <span data-ttu-id="eee50-121">Manıza</span><span class="sxs-lookup"><span data-stu-id="eee50-121">Ignore</span></span>
- <span data-ttu-id="eee50-122">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="eee50-122">Inquire</span></span>
- <span data-ttu-id="eee50-123">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="eee50-123">SilentlyContinue</span></span>
- <span data-ttu-id="eee50-124">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="eee50-124">Stop</span></span>
- <span data-ttu-id="eee50-125">Biliriz</span><span class="sxs-lookup"><span data-stu-id="eee50-125">Suspend</span></span>

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

### <span data-ttu-id="eee50-126">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="eee50-126">-InformationVariable</span></span>
<span data-ttu-id="eee50-127">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eee50-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="eee50-128">-Profile</span></span>
<span data-ttu-id="eee50-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eee50-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="eee50-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eee50-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="eee50-131">-ProviderNamespace</span></span>
<span data-ttu-id="eee50-132">Uzantı sağlayıcı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee50-133">-Role</span><span class="sxs-lookup"><span data-stu-id="eee50-133">-Role</span></span>
<span data-ttu-id="eee50-134">Uzantısını belirtmek için isteğe bağlı bir rol dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="eee50-135">Belirtilmezse, uzantı tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="eee50-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="eee50-136">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="eee50-136">-ServiceName</span></span>
<span data-ttu-id="eee50-137">Bulut hizmeti adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="eee50-138">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="eee50-138">-Slot</span></span>
<span data-ttu-id="eee50-139">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee50-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="eee50-140">Geçerli değerler üretim veya aşamalardır.</span><span class="sxs-lookup"><span data-stu-id="eee50-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="eee50-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="eee50-141">-UninstallConfiguration</span></span>
<span data-ttu-id="eee50-142">Bu cmdlet 'in bulut hizmetindeki tüm yapılandırmaları kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eee50-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee50-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee50-143">CommonParameters</span></span>
<span data-ttu-id="eee50-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eee50-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee50-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee50-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee50-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eee50-146">INPUTS</span></span>

## <span data-ttu-id="eee50-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eee50-147">OUTPUTS</span></span>

## <span data-ttu-id="eee50-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eee50-148">NOTES</span></span>

## <span data-ttu-id="eee50-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eee50-149">RELATED LINKS</span></span>

[<span data-ttu-id="eee50-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="eee50-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="eee50-151">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="eee50-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


