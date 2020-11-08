---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106091"
---
# <span data-ttu-id="48581-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48581-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="48581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48581-102">SYNOPSIS</span></span>
<span data-ttu-id="48581-103">Traffic Manager profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48581-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="48581-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48581-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="48581-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48581-105">DESCRIPTION</span></span>
<span data-ttu-id="48581-106">**Remove-AzureTrafficManagerProfile** cmdlet 'i geçerli abonelikteki bir Microsoft Azure Traffic Manager profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48581-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="48581-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48581-107">EXAMPLES</span></span>

### <span data-ttu-id="48581-108">Örnek 1: Traffic Manager profilini kaldırma</span><span class="sxs-lookup"><span data-stu-id="48581-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="48581-109">Bu komut Myprofıle adlı Traffic Manager profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48581-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="48581-110">Örnek 2: Traffic Manager profilini kaldırma</span><span class="sxs-lookup"><span data-stu-id="48581-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="48581-111">Bu komut Myprofıle adlı Traffic Manager profilini onaylamanızı istemeden kaldırır ve sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="48581-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="48581-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48581-112">PARAMETERS</span></span>

### <span data-ttu-id="48581-113">-Force</span><span class="sxs-lookup"><span data-stu-id="48581-113">-Force</span></span>
<span data-ttu-id="48581-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="48581-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48581-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="48581-115">-Name</span></span>
<span data-ttu-id="48581-116">Silinecek Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48581-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="48581-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="48581-117">-PassThru</span></span>
<span data-ttu-id="48581-118">İşlem başarılı olursa $True döndürür; Aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="48581-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="48581-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="48581-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48581-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="48581-120">-Profile</span></span>
<span data-ttu-id="48581-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48581-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="48581-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="48581-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48581-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48581-123">CommonParameters</span></span>
<span data-ttu-id="48581-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48581-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48581-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48581-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48581-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48581-126">INPUTS</span></span>

## <span data-ttu-id="48581-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48581-127">OUTPUTS</span></span>

### <span data-ttu-id="48581-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48581-128">System.Boolean</span></span>
<span data-ttu-id="48581-129">Bu cmdlet $True veya $False oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48581-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="48581-130">İşlem başarılıysa ve *geçiş parametresini belirtirseniz, bu* cmdlet bir $true değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="48581-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="48581-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48581-131">NOTES</span></span>

## <span data-ttu-id="48581-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48581-132">RELATED LINKS</span></span>

[<span data-ttu-id="48581-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48581-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="48581-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48581-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="48581-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48581-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="48581-136">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48581-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="48581-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48581-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


