---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105480"
---
# <span data-ttu-id="d564e-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="d564e-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="d564e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d564e-102">SYNOPSIS</span></span>
<span data-ttu-id="d564e-103">Tek bir rol örneğinin veya belirli bir rolün tüm rol örneklerinin yeniden başlatılmasını veya yeniden yansımasını ister.</span><span class="sxs-lookup"><span data-stu-id="d564e-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="d564e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d564e-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d564e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d564e-105">DESCRIPTION</span></span>
<span data-ttu-id="d564e-106">**Reset-Azureroleınstance** cmdlet 'i, dağıtımda çalışan bir rol örneğinin yeniden başlatılmasını veya yeniden yansımasını ister.</span><span class="sxs-lookup"><span data-stu-id="d564e-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="d564e-107">Bu işlem eşzamanlı olarak yürütülür.</span><span class="sxs-lookup"><span data-stu-id="d564e-107">This operation executes synchronously.</span></span>
<span data-ttu-id="d564e-108">Bir rol örneğini yeniden başlattığınızda, Azure bu örneği çevrimdışı olarak alır, bu örnek için temel işletim sistemini yeniden başlatır ve örneği çevrimiçi duruma getirir.</span><span class="sxs-lookup"><span data-stu-id="d564e-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="d564e-109">Yerel diske yazılan tüm veriler yeniden başlatmalar genelinde devam edilir.</span><span class="sxs-lookup"><span data-stu-id="d564e-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="d564e-110">Bellekteki veriler kaybedilir.</span><span class="sxs-lookup"><span data-stu-id="d564e-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="d564e-111">Rol örneği yeniden Imaging rol türüne bağlı olarak farklı davranışlara neden olacak.</span><span class="sxs-lookup"><span data-stu-id="d564e-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="d564e-112">Web veya işçi rolünde, rol yeniden görüntülendiğinde, Azure rolü çevrimdışı olarak alır ve sanal makineye Azure Konuk işletim sisteminin yeni yüklemesini yazar.</span><span class="sxs-lookup"><span data-stu-id="d564e-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="d564e-113">Rol yeniden çevrimiçi duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="d564e-113">The role is then brought back online.</span></span>
<span data-ttu-id="d564e-114">VM rolü için, rol yeniden görüntülendiğinde, Azure rolü çevrimdışı olarak alır, onun için sağladığınız özel resmi yeniden uygular ve rolü çevrimiçine geri getirir.</span><span class="sxs-lookup"><span data-stu-id="d564e-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="d564e-115">Azure, rol yeniden görüntülendiğinde yerel depolama kaynaklarındaki verileri bakımını yapmaya çalışır; Ancak, geçici bir donanım arızası durumunda, yerel depolama kaynağı kaybolabilir.</span><span class="sxs-lookup"><span data-stu-id="d564e-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="d564e-116">Uygulamanız verilerin kalıcı olmasını gerektiriyorsa, Azure sürücüsü gibi dayanıklı bir veri kaynağına yazma önerilir.</span><span class="sxs-lookup"><span data-stu-id="d564e-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="d564e-117">Yerel depolama kaynağı tarafından tanımlandıkları yerel dizine yazılan tüm veriler, rol yeniden görüntülendiğinde kaybedilir.</span><span class="sxs-lookup"><span data-stu-id="d564e-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="d564e-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d564e-118">EXAMPLES</span></span>

### <span data-ttu-id="d564e-119">Örnek 1: rol örneğini yeniden yükleme</span><span class="sxs-lookup"><span data-stu-id="d564e-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="d564e-120">Bu komut, MySvc01 hizmetinin hazırlama dağıtımında MyWebRole_IN_0 adlı rol örneğini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d564e-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="d564e-121">Örnek 2: bir rol örneğini yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="d564e-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="d564e-122">Bu komut, MySvc01 bulut hizmetinin hazırlama dağıtımında rol örneklerini yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d564e-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="d564e-123">Örnek 3: tüm rol örneklerini yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="d564e-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="d564e-124">Bu komut, MySvc01 hizmetinin üretim dağıtımındaki tüm rol örneklerini yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d564e-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="d564e-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d564e-125">PARAMETERS</span></span>

### <span data-ttu-id="d564e-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d564e-126">-InformationAction</span></span>
<span data-ttu-id="d564e-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d564e-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d564e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d564e-129">'A</span><span class="sxs-lookup"><span data-stu-id="d564e-129">Continue</span></span>
- <span data-ttu-id="d564e-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="d564e-130">Ignore</span></span>
- <span data-ttu-id="d564e-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d564e-131">Inquire</span></span>
- <span data-ttu-id="d564e-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d564e-132">SilentlyContinue</span></span>
- <span data-ttu-id="d564e-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d564e-133">Stop</span></span>
- <span data-ttu-id="d564e-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d564e-134">Suspend</span></span>

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

### <span data-ttu-id="d564e-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d564e-135">-InformationVariable</span></span>
<span data-ttu-id="d564e-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d564e-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d564e-137">-InstanceName</span></span>
<span data-ttu-id="d564e-138">Yeniden görüntü veya yeniden başlatma için rol örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564e-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="d564e-139">-Profile</span></span>
<span data-ttu-id="d564e-140">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d564e-141">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d564e-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d564e-142">-Reboot</span><span class="sxs-lookup"><span data-stu-id="d564e-142">-Reboot</span></span>
<span data-ttu-id="d564e-143">Bu cmdlet 'in belirtilen rol örneğini veya belirtilmemişse, tüm rol örneklerini yeniden önolduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="d564e-144">*Yeniden başlatma* veya *yeniden görüntü* parametresi eklemeniz gerekir, ancak ikisini birden içeremez.</span><span class="sxs-lookup"><span data-stu-id="d564e-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564e-145">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="d564e-145">-Reimage</span></span>
<span data-ttu-id="d564e-146">Bu cmdlet 'in belirtilen rol örneğinin veya belirtilmemişse, tüm rol örneklerinin yeniden yansımasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="d564e-147">*Yeniden başlatma* veya *yeniden görüntü* parametresi eklemeniz gerekir, ancak ikisini birden içeremez.</span><span class="sxs-lookup"><span data-stu-id="d564e-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564e-148">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d564e-148">-ServiceName</span></span>
<span data-ttu-id="d564e-149">Hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-149">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="d564e-150">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d564e-150">-Slot</span></span>
<span data-ttu-id="d564e-151">Rol örneklerinin çalıştırdığı dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d564e-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="d564e-152">Geçerli değerler: üretim ve hazırlama.</span><span class="sxs-lookup"><span data-stu-id="d564e-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="d564e-153">*DeploymentName* veya *yuva* parametresini ekleyebilirsiniz, ancak ikisini birden içeremez.</span><span class="sxs-lookup"><span data-stu-id="d564e-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d564e-154">CommonParameters</span></span>
<span data-ttu-id="d564e-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d564e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d564e-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d564e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d564e-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d564e-157">INPUTS</span></span>

## <span data-ttu-id="d564e-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d564e-158">OUTPUTS</span></span>

## <span data-ttu-id="d564e-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d564e-159">NOTES</span></span>

## <span data-ttu-id="d564e-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d564e-160">RELATED LINKS</span></span>

[<span data-ttu-id="d564e-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="d564e-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


