---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106331"
---
# <span data-ttu-id="fcafb-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="fcafb-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="fcafb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcafb-102">SYNOPSIS</span></span>
<span data-ttu-id="fcafb-103">Bir Azure sanal makinesinin genel IP bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcafb-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="fcafb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcafb-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fcafb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcafb-105">DESCRIPTION</span></span>
<span data-ttu-id="fcafb-106">**Get-AzurePublicIP** cmdlet 'ı bir Azure sanal MAKINESININ genel IP bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcafb-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="fcafb-107">Genel IP adresini almak için **Get-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fcafb-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="fcafb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcafb-108">EXAMPLES</span></span>

### <span data-ttu-id="fcafb-109">Örnek 1: genel IP yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="fcafb-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="fcafb-110">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak Ftpınazure adlı hizmette ftpınstance adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="fcafb-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="fcafb-111">Komut, ardışık düzen işlecini kullanarak bu sanal makineyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="fcafb-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fcafb-112">Geçerli cmdlet, sanal makineden ortak IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="fcafb-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="fcafb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcafb-113">PARAMETERS</span></span>

### <span data-ttu-id="fcafb-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fcafb-114">-InformationAction</span></span>
<span data-ttu-id="fcafb-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcafb-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fcafb-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fcafb-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcafb-117">'A</span><span class="sxs-lookup"><span data-stu-id="fcafb-117">Continue</span></span>
- <span data-ttu-id="fcafb-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="fcafb-118">Ignore</span></span>
- <span data-ttu-id="fcafb-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fcafb-119">Inquire</span></span>
- <span data-ttu-id="fcafb-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fcafb-120">SilentlyContinue</span></span>
- <span data-ttu-id="fcafb-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fcafb-121">Stop</span></span>
- <span data-ttu-id="fcafb-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fcafb-122">Suspend</span></span>

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

### <span data-ttu-id="fcafb-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fcafb-123">-InformationVariable</span></span>
<span data-ttu-id="fcafb-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcafb-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fcafb-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="fcafb-125">-Profile</span></span>
<span data-ttu-id="fcafb-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcafb-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcafb-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fcafb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcafb-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="fcafb-128">-PublicIPName</span></span>
<span data-ttu-id="fcafb-129">Genel IP adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcafb-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="fcafb-130">-VM</span><span class="sxs-lookup"><span data-stu-id="fcafb-130">-VM</span></span>
<span data-ttu-id="fcafb-131">Bu cmdlet 'in genel IP yapılandırmasını aldığı sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcafb-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcafb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcafb-132">CommonParameters</span></span>
<span data-ttu-id="fcafb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcafb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcafb-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcafb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcafb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcafb-135">INPUTS</span></span>

## <span data-ttu-id="fcafb-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcafb-136">OUTPUTS</span></span>

### <span data-ttu-id="fcafb-137">Microsoft. Windowsazde. Commands. ServiceManagement. Atamaaddercollection</span><span class="sxs-lookup"><span data-stu-id="fcafb-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="fcafb-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcafb-138">NOTES</span></span>

## <span data-ttu-id="fcafb-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcafb-139">RELATED LINKS</span></span>

[<span data-ttu-id="fcafb-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fcafb-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fcafb-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="fcafb-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="fcafb-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="fcafb-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


