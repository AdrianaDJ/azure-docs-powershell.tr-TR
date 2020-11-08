---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106375"
---
# <span data-ttu-id="71ec6-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71ec6-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="71ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="71ec6-103">Traffic Manager profili etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="71ec6-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="71ec6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71ec6-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="71ec6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="71ec6-106">**Enable-AzureTrafficManagerProfile** cmdlet 'ı bir Microsoft Azure Traffic Manager profili sağlar.</span><span class="sxs-lookup"><span data-stu-id="71ec6-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="71ec6-107">İşlemin başarılı olup olmadığını göstermek için *geçiş parametresini belirtin* .</span><span class="sxs-lookup"><span data-stu-id="71ec6-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="71ec6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71ec6-108">EXAMPLES</span></span>

### <span data-ttu-id="71ec6-109">Örnek 1: Traffic Manager profilini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="71ec6-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="71ec6-110">Bu komut Myprofıle adlı Traffic Manager profilini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="71ec6-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="71ec6-111">Örnek 2: Traffic Manager profilini etkinleştirme ve sonuçları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="71ec6-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="71ec6-112">Bu komut Myprofıle adlı Traffic Manager profilini ve komutun başarılı olup olmadığını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="71ec6-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="71ec6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71ec6-113">PARAMETERS</span></span>

### <span data-ttu-id="71ec6-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="71ec6-114">-Name</span></span>
<span data-ttu-id="71ec6-115">Etkinleştirilecek Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71ec6-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="71ec6-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="71ec6-116">-PassThru</span></span>
<span data-ttu-id="71ec6-117">İşlem başarılı olursa $True döndürür; Aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="71ec6-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="71ec6-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="71ec6-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ec6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="71ec6-119">-Profile</span></span>
<span data-ttu-id="71ec6-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71ec6-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="71ec6-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="71ec6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71ec6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ec6-122">CommonParameters</span></span>
<span data-ttu-id="71ec6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71ec6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ec6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ec6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ec6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71ec6-125">INPUTS</span></span>

## <span data-ttu-id="71ec6-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71ec6-126">OUTPUTS</span></span>

### <span data-ttu-id="71ec6-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71ec6-127">System.Boolean</span></span>
<span data-ttu-id="71ec6-128">Bu cmdlet $True veya $False oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71ec6-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="71ec6-129">İşlem başarılı olursa ve *geçiş parametresini belirtirseniz, bu* cmdlet bir $true değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="71ec6-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="71ec6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71ec6-130">NOTES</span></span>

## <span data-ttu-id="71ec6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71ec6-131">RELATED LINKS</span></span>

[<span data-ttu-id="71ec6-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71ec6-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="71ec6-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71ec6-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="71ec6-134">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71ec6-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="71ec6-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71ec6-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="71ec6-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="71ec6-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


