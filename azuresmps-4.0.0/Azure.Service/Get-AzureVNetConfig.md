---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106288"
---
# <span data-ttu-id="189c2-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="189c2-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="189c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="189c2-102">SYNOPSIS</span></span>
<span data-ttu-id="189c2-103">Geçerli abonelikten Azure sanal ağ yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="189c2-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="189c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="189c2-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="189c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="189c2-105">DESCRIPTION</span></span>
<span data-ttu-id="189c2-106">**Get-AzureVNetConfig** cmdlet 'i, geçerli Azure aboneliğinin sanal ağ yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="189c2-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="189c2-107">*Exporttofile* parametresi belirtilmişse, bir ağ yapılandırma dosyası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="189c2-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="189c2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="189c2-108">EXAMPLES</span></span>

### <span data-ttu-id="189c2-109">Örnek 1: geçerli Azure aboneliğinin sanal ağ yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="189c2-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="189c2-110">Bu komut, geçerli Azure aboneliğinin sanal ağ yapılandırmasını alır ve görüntüler.</span><span class="sxs-lookup"><span data-stu-id="189c2-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="189c2-111">Örnek 2: geçerli Azure aboneliğinin sanal ağ yapılandırmasını alma ve yerel dosyaya kaydetme</span><span class="sxs-lookup"><span data-stu-id="189c2-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="189c2-112">Bu komut, geçerli Azure aboneliğinin sanal ağ yapılandırmasını alır ve bir yerel dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="189c2-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="189c2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="189c2-113">PARAMETERS</span></span>

### <span data-ttu-id="189c2-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="189c2-114">-ExportToFile</span></span>
<span data-ttu-id="189c2-115">Ayarlardan oluşturulacak ağ yapılandırma dosyasının yolunu ve dosya adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="189c2-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="189c2-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="189c2-116">-InformationAction</span></span>
<span data-ttu-id="189c2-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="189c2-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="189c2-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="189c2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="189c2-119">'A</span><span class="sxs-lookup"><span data-stu-id="189c2-119">Continue</span></span>
- <span data-ttu-id="189c2-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="189c2-120">Ignore</span></span>
- <span data-ttu-id="189c2-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="189c2-121">Inquire</span></span>
- <span data-ttu-id="189c2-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="189c2-122">SilentlyContinue</span></span>
- <span data-ttu-id="189c2-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="189c2-123">Stop</span></span>
- <span data-ttu-id="189c2-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="189c2-124">Suspend</span></span>

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

### <span data-ttu-id="189c2-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="189c2-125">-InformationVariable</span></span>
<span data-ttu-id="189c2-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="189c2-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="189c2-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="189c2-127">-Profile</span></span>
<span data-ttu-id="189c2-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="189c2-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="189c2-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="189c2-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="189c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189c2-130">CommonParameters</span></span>
<span data-ttu-id="189c2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="189c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189c2-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="189c2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189c2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="189c2-133">INPUTS</span></span>

## <span data-ttu-id="189c2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="189c2-134">OUTPUTS</span></span>

## <span data-ttu-id="189c2-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="189c2-135">NOTES</span></span>

## <span data-ttu-id="189c2-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="189c2-136">RELATED LINKS</span></span>

[<span data-ttu-id="189c2-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="189c2-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="189c2-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="189c2-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="189c2-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="189c2-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


