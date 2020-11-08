---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106116"
---
# <span data-ttu-id="73c5a-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73c5a-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="73c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="73c5a-103">Belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73c5a-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="73c5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73c5a-104">SYNTAX</span></span>

### <span data-ttu-id="73c5a-105">RemoveByRoles (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73c5a-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="73c5a-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="73c5a-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="73c5a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="73c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="73c5a-108">**Remove-Azurezervicediagnoksextensextencmdlet** 'i, belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti Tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73c5a-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="73c5a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="73c5a-110">Örnek 1: hizmetin tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73c5a-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="73c5a-111">Bu komut belirtilen rolün tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73c5a-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="73c5a-112">Örnek 2: belirtilen rolde hizmetin tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73c5a-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="73c5a-113">Bu komut belirtilen rolün tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73c5a-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="73c5a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73c5a-114">PARAMETERS</span></span>

### <span data-ttu-id="73c5a-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="73c5a-115">-InformationAction</span></span>
<span data-ttu-id="73c5a-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="73c5a-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="73c5a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73c5a-118">'A</span><span class="sxs-lookup"><span data-stu-id="73c5a-118">Continue</span></span>
- <span data-ttu-id="73c5a-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="73c5a-119">Ignore</span></span>
- <span data-ttu-id="73c5a-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="73c5a-120">Inquire</span></span>
- <span data-ttu-id="73c5a-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="73c5a-121">SilentlyContinue</span></span>
- <span data-ttu-id="73c5a-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="73c5a-122">Stop</span></span>
- <span data-ttu-id="73c5a-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="73c5a-123">Suspend</span></span>

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

### <span data-ttu-id="73c5a-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="73c5a-124">-InformationVariable</span></span>
<span data-ttu-id="73c5a-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="73c5a-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="73c5a-126">-Profile</span></span>
<span data-ttu-id="73c5a-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73c5a-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="73c5a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73c5a-129">-Role</span><span class="sxs-lookup"><span data-stu-id="73c5a-129">-Role</span></span>
<span data-ttu-id="73c5a-130">Uzak Masaüstü yapılandırmasının belirtilmesi için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="73c5a-131">Bu parametreyi belirtmezseniz, uzak masaüstü yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="73c5a-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="73c5a-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="73c5a-132">-ServiceName</span></span>
<span data-ttu-id="73c5a-133">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="73c5a-134">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="73c5a-134">-Slot</span></span>
<span data-ttu-id="73c5a-135">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="73c5a-136">Geçerli değerler üretim veya aşamalardır.</span><span class="sxs-lookup"><span data-stu-id="73c5a-136">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="73c5a-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="73c5a-137">-UninstallConfiguration</span></span>
<span data-ttu-id="73c5a-138">Bu cmdlet 'in bulut hizmetindeki tüm RDP yapılandırmalarını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73c5a-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="73c5a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c5a-139">CommonParameters</span></span>
<span data-ttu-id="73c5a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73c5a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c5a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c5a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c5a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73c5a-142">INPUTS</span></span>

## <span data-ttu-id="73c5a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73c5a-143">OUTPUTS</span></span>

## <span data-ttu-id="73c5a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73c5a-144">NOTES</span></span>

## <span data-ttu-id="73c5a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73c5a-145">RELATED LINKS</span></span>

[<span data-ttu-id="73c5a-146">Get-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="73c5a-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="73c5a-147">Set-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="73c5a-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


