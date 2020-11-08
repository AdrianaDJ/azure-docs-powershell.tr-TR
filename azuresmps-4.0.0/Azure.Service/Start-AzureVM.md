---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105771"
---
# <span data-ttu-id="2945a-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2945a-101">Start-AzureVM</span></span>

## <span data-ttu-id="2945a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2945a-102">SYNOPSIS</span></span>
<span data-ttu-id="2945a-103">Azure sanal makinesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="2945a-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="2945a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2945a-104">SYNTAX</span></span>

### <span data-ttu-id="2945a-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2945a-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2945a-106">Girdiden</span><span class="sxs-lookup"><span data-stu-id="2945a-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2945a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2945a-107">DESCRIPTION</span></span>
<span data-ttu-id="2945a-108">**Start-AzureVM** cmdlet 'ı bir Azure sanal makinesinin başlangıcını ister.</span><span class="sxs-lookup"><span data-stu-id="2945a-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="2945a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2945a-109">EXAMPLES</span></span>

### <span data-ttu-id="2945a-110">Örnek 1: sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="2945a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="2945a-111">Bu komut, ContosoService03 adındaki Azure hizmetinde çalışan VirtualMachine04 adındaki sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2945a-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="2945a-112">Örnek 2: sanal makine nesnesi kullanarak sanal makine başlatma</span><span class="sxs-lookup"><span data-stu-id="2945a-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="2945a-113">Bu komut, adı DatabaseServer olan sanal makinenin sanal makine nesnesini alır ve ardından başlatma isteğinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="2945a-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="2945a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2945a-114">PARAMETERS</span></span>

### <span data-ttu-id="2945a-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2945a-115">-InformationAction</span></span>
<span data-ttu-id="2945a-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2945a-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2945a-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2945a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2945a-118">'A</span><span class="sxs-lookup"><span data-stu-id="2945a-118">Continue</span></span>
- <span data-ttu-id="2945a-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="2945a-119">Ignore</span></span>
- <span data-ttu-id="2945a-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2945a-120">Inquire</span></span>
- <span data-ttu-id="2945a-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2945a-121">SilentlyContinue</span></span>
- <span data-ttu-id="2945a-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2945a-122">Stop</span></span>
- <span data-ttu-id="2945a-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2945a-123">Suspend</span></span>

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

### <span data-ttu-id="2945a-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2945a-124">-InformationVariable</span></span>
<span data-ttu-id="2945a-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2945a-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2945a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2945a-126">-Name</span></span>
<span data-ttu-id="2945a-127">Başlayacak sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2945a-127">Specifies the name of the virtual machine to start.</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2945a-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="2945a-128">-Profile</span></span>
<span data-ttu-id="2945a-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2945a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2945a-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2945a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2945a-131">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="2945a-131">-ServiceName</span></span>
<span data-ttu-id="2945a-132">Başlayacak sanal makineyi içeren Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2945a-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="2945a-133">-VM</span><span class="sxs-lookup"><span data-stu-id="2945a-133">-VM</span></span>
<span data-ttu-id="2945a-134">Başlayacak sanal makineyi tanımlayan sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2945a-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2945a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2945a-135">CommonParameters</span></span>
<span data-ttu-id="2945a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2945a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2945a-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2945a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2945a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2945a-138">INPUTS</span></span>

## <span data-ttu-id="2945a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2945a-139">OUTPUTS</span></span>

## <span data-ttu-id="2945a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2945a-140">NOTES</span></span>

## <span data-ttu-id="2945a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2945a-141">RELATED LINKS</span></span>

[<span data-ttu-id="2945a-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2945a-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="2945a-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2945a-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="2945a-144">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2945a-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="2945a-145">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2945a-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="2945a-146">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2945a-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


