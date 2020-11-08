---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105620"
---
# <span data-ttu-id="b8202-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="b8202-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="b8202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8202-102">SYNOPSIS</span></span>
<span data-ttu-id="b8202-103">Bir Azure sanal makinesi için RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="b8202-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="b8202-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8202-104">SYNTAX</span></span>

### <span data-ttu-id="b8202-105">İndir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8202-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8202-106">Başlatılması</span><span class="sxs-lookup"><span data-stu-id="b8202-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8202-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8202-107">DESCRIPTION</span></span>
<span data-ttu-id="b8202-108">**Get-AzureRemoteDesktopFile** cmdlet 'i, bir Azure sanal makinesi için bir uzak masaüstü BAĞLANTıSı (RDP) dosyası indirip kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b8202-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="b8202-109">Cmdlet, belirtilen sanal makineye bir Uzak Masaüstü bağlantısı başlatabilir.</span><span class="sxs-lookup"><span data-stu-id="b8202-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="b8202-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8202-110">EXAMPLES</span></span>

### <span data-ttu-id="b8202-111">Örnek 1: RDP dosyası alma</span><span class="sxs-lookup"><span data-stu-id="b8202-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="b8202-112">Bu komut, ContosoService adlı hizmette çalışan VirtualMachine07 adındaki VirtualMachine07 sanal makinesi için bir RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="b8202-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="b8202-113">Komut bu dosyayı C:\temp\virtualmachine07.rdpadıyla depolar.</span><span class="sxs-lookup"><span data-stu-id="b8202-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="b8202-114">Örnek 2: uzak oturum başlatma</span><span class="sxs-lookup"><span data-stu-id="b8202-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="b8202-115">Bu komut, ContosoService adlı hizmette çalışan VirtualMachine07 adındaki VirtualMachine07 sanal makinesi için bir RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="b8202-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="b8202-116">Komut bir Uzak Masaüstü oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="b8202-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="b8202-117">Komut, bağlantı kapalıyken RDP dosyasını siler.</span><span class="sxs-lookup"><span data-stu-id="b8202-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="b8202-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8202-118">PARAMETERS</span></span>

### <span data-ttu-id="b8202-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b8202-119">-InformationAction</span></span>
<span data-ttu-id="b8202-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8202-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8202-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b8202-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8202-122">'A</span><span class="sxs-lookup"><span data-stu-id="b8202-122">Continue</span></span>
- <span data-ttu-id="b8202-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="b8202-123">Ignore</span></span>
- <span data-ttu-id="b8202-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b8202-124">Inquire</span></span>
- <span data-ttu-id="b8202-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b8202-125">SilentlyContinue</span></span>
- <span data-ttu-id="b8202-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b8202-126">Stop</span></span>
- <span data-ttu-id="b8202-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b8202-127">Suspend</span></span>

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

### <span data-ttu-id="b8202-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b8202-128">-InformationVariable</span></span>
<span data-ttu-id="b8202-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8202-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b8202-130">-Başlat</span><span class="sxs-lookup"><span data-stu-id="b8202-130">-Launch</span></span>
<span data-ttu-id="b8202-131">Bu cmdlet 'in sanal makineye bir Uzak Masaüstü oturumu başladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8202-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8202-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="b8202-132">-LocalPath</span></span>
<span data-ttu-id="b8202-133">Yerel bilgisayarda indirilen RDP dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8202-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8202-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8202-134">-Name</span></span>
<span data-ttu-id="b8202-135">Bu cmdlet 'in RDP dosyasını yüklediği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8202-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8202-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8202-136">-Profile</span></span>
<span data-ttu-id="b8202-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8202-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8202-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b8202-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8202-139">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="b8202-139">-ServiceName</span></span>
<span data-ttu-id="b8202-140">Sanal makinenin ait olduğu Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8202-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="b8202-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8202-141">CommonParameters</span></span>
<span data-ttu-id="b8202-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8202-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8202-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8202-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8202-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8202-144">INPUTS</span></span>

## <span data-ttu-id="b8202-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8202-145">OUTPUTS</span></span>

## <span data-ttu-id="b8202-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8202-146">NOTES</span></span>

## <span data-ttu-id="b8202-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8202-147">RELATED LINKS</span></span>

