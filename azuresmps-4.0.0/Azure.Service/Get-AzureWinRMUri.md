---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106505"
---
# <span data-ttu-id="647f1-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="647f1-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="647f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="647f1-102">SYNOPSIS</span></span>
<span data-ttu-id="647f1-103">Bir sanal makineye veya barındırılan hizmette bulunan sanal makinelerin listesine WinRM HTTPS dinleyicisi URI 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="647f1-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="647f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="647f1-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="647f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="647f1-105">DESCRIPTION</span></span>
<span data-ttu-id="647f1-106">**Get-AzureWinRMUri** cmdlet 'ı, Windows Uzaktan Yönetim (WinRM) https DINLEYICISININ URI 'sini sanal makineye veya barındırılan hizmette sanal makinelerin listesine alır.</span><span class="sxs-lookup"><span data-stu-id="647f1-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="647f1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="647f1-107">EXAMPLES</span></span>

### <span data-ttu-id="647f1-108">Örnek 1: sanal makineye WinRM HTTPS dinleyicisi URI 'sini alma</span><span class="sxs-lookup"><span data-stu-id="647f1-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="647f1-109">Bu komut, WinRM HTTPS dinleyicisinin sanal makineye uar düzeyini alır.</span><span class="sxs-lookup"><span data-stu-id="647f1-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="647f1-110">Örnek 2: belirli bir hizmetin sanal makinesine WinRM HTTPS dinleyicisi URI 'sini alma</span><span class="sxs-lookup"><span data-stu-id="647f1-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="647f1-111">Bu komut, WinRM HTTPS dinleyicisinin sanal makineye uar düzeyini alır.</span><span class="sxs-lookup"><span data-stu-id="647f1-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="647f1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="647f1-112">PARAMETERS</span></span>

### <span data-ttu-id="647f1-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="647f1-113">-InformationAction</span></span>
<span data-ttu-id="647f1-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="647f1-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="647f1-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="647f1-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="647f1-116">'A</span><span class="sxs-lookup"><span data-stu-id="647f1-116">Continue</span></span>
- <span data-ttu-id="647f1-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="647f1-117">Ignore</span></span>
- <span data-ttu-id="647f1-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="647f1-118">Inquire</span></span>
- <span data-ttu-id="647f1-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="647f1-119">SilentlyContinue</span></span>
- <span data-ttu-id="647f1-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="647f1-120">Stop</span></span>
- <span data-ttu-id="647f1-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="647f1-121">Suspend</span></span>

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

### <span data-ttu-id="647f1-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="647f1-122">-InformationVariable</span></span>
<span data-ttu-id="647f1-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="647f1-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="647f1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="647f1-124">-Name</span></span>
<span data-ttu-id="647f1-125">WinRM URI 'sinin oluşturulduğu sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="647f1-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

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

### <span data-ttu-id="647f1-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="647f1-126">-Profile</span></span>
<span data-ttu-id="647f1-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="647f1-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="647f1-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="647f1-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="647f1-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="647f1-129">-ServiceName</span></span>
<span data-ttu-id="647f1-130">Sanal makineyi barındıran Microsoft Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="647f1-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="647f1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647f1-131">CommonParameters</span></span>
<span data-ttu-id="647f1-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="647f1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647f1-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="647f1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647f1-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="647f1-134">INPUTS</span></span>

## <span data-ttu-id="647f1-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="647f1-135">OUTPUTS</span></span>

## <span data-ttu-id="647f1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="647f1-136">NOTES</span></span>

## <span data-ttu-id="647f1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="647f1-137">RELATED LINKS</span></span>

[<span data-ttu-id="647f1-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="647f1-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="647f1-139">Yeni-Azutalep Ickvm</span><span class="sxs-lookup"><span data-stu-id="647f1-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


