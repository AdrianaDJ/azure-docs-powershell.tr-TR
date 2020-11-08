---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106112"
---
# <span data-ttu-id="4c49a-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="4c49a-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="4c49a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c49a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c49a-103">Belirtilen dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti uzak masaüstü uzantısı 'nı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c49a-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="4c49a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c49a-104">SYNTAX</span></span>

### <span data-ttu-id="4c49a-105">RemoveByRoles (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c49a-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c49a-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="4c49a-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4c49a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c49a-107">DESCRIPTION</span></span>
<span data-ttu-id="4c49a-108">**Remove-Azurezerviceremotedesktopextension** cmdlet 'i, belirli bir dağıtım yuvasında tüm rollere veya adlandırılmış rollere uygulanan bulut hizmeti uzak masaüstü uzantısı 'nı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c49a-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="4c49a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c49a-109">EXAMPLES</span></span>

### <span data-ttu-id="4c49a-110">Örnek 1: Uzak Masaüstü uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c49a-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="4c49a-111">Bu komut, Uzak Masaüstü uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c49a-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="4c49a-112">Örnek 2: belirtilen rolden Uzak Masaüstü uzantısı 'nı kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c49a-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="4c49a-113">Bu komut, belirtilen rolden Uzak Masaüstü uzantısı 'nı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c49a-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="4c49a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c49a-114">PARAMETERS</span></span>

### <span data-ttu-id="4c49a-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4c49a-115">-InformationAction</span></span>
<span data-ttu-id="4c49a-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4c49a-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c49a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c49a-118">'A</span><span class="sxs-lookup"><span data-stu-id="4c49a-118">Continue</span></span>
- <span data-ttu-id="4c49a-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="4c49a-119">Ignore</span></span>
- <span data-ttu-id="4c49a-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="4c49a-120">Inquire</span></span>
- <span data-ttu-id="4c49a-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="4c49a-121">SilentlyContinue</span></span>
- <span data-ttu-id="4c49a-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="4c49a-122">Stop</span></span>
- <span data-ttu-id="4c49a-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="4c49a-123">Suspend</span></span>

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

### <span data-ttu-id="4c49a-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="4c49a-124">-InformationVariable</span></span>
<span data-ttu-id="4c49a-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4c49a-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c49a-126">-Profile</span></span>
<span data-ttu-id="4c49a-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c49a-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4c49a-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c49a-129">-Role</span><span class="sxs-lookup"><span data-stu-id="4c49a-129">-Role</span></span>
<span data-ttu-id="4c49a-130">Uzak Masaüstü yapılandırmasını belirtmek için isteğe bağlı bir rol dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="4c49a-131">Belirtilmezse, uzak masaüstü yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4c49a-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="4c49a-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="4c49a-132">-ServiceName</span></span>
<span data-ttu-id="4c49a-133">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="4c49a-134">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4c49a-134">-Slot</span></span>
<span data-ttu-id="4c49a-135">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="4c49a-136">Desteklenen değerler "üretim" veya "aşamalandırma".</span><span class="sxs-lookup"><span data-stu-id="4c49a-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="4c49a-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c49a-137">-UninstallConfiguration</span></span>
<span data-ttu-id="4c49a-138">Bu cmdlet 'in bulut hizmetindeki tüm RDP yapılandırmalarını kaldırıp bu cmdlet 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c49a-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="4c49a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c49a-139">CommonParameters</span></span>
<span data-ttu-id="4c49a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c49a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c49a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c49a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c49a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c49a-142">INPUTS</span></span>

## <span data-ttu-id="4c49a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c49a-143">OUTPUTS</span></span>

## <span data-ttu-id="4c49a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c49a-144">NOTES</span></span>

## <span data-ttu-id="4c49a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c49a-145">RELATED LINKS</span></span>

[<span data-ttu-id="4c49a-146">Set-Azurezerviceremotedesktopextension</span><span class="sxs-lookup"><span data-stu-id="4c49a-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


