---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105693"
---
# <span data-ttu-id="d8d87-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d87-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="d8d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d87-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d87-103">Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d8d87-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="d8d87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8d87-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8d87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8d87-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d87-106">**Disable-AzureTrafficManagerProfile** cmdlet 'ı bir Microsoft Azure Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d8d87-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d8d87-107">İşlemin başarılı olup olmadığını görüntülemek için *geçiş parametresini kullanabilirsiniz* .</span><span class="sxs-lookup"><span data-stu-id="d8d87-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="d8d87-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8d87-108">EXAMPLES</span></span>

### <span data-ttu-id="d8d87-109">Örnek 1: Traffic Manager profilini devre dışı bırakma ve sonuçları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d8d87-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="d8d87-110">Bu komut Myprofıle adlı Traffic Manager profilini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d8d87-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="d8d87-111">Komut, komutun başarılı olup olmadığını göstermek için *geçiş parametresini belirtir* .</span><span class="sxs-lookup"><span data-stu-id="d8d87-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="d8d87-112">Örnek 2: Traffic Manager profilini devre dışı bırakma ve sonuç görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d8d87-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="d8d87-113">Bu komut Myprofıle adlı Traffic Manager profilini devre dışı bırakır ancak komutun başarılı olup olmadığını görüntülemez.</span><span class="sxs-lookup"><span data-stu-id="d8d87-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="d8d87-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8d87-114">PARAMETERS</span></span>

### <span data-ttu-id="d8d87-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8d87-115">-Name</span></span>
<span data-ttu-id="d8d87-116">Devre dışı bırakmak için Traffic Manager profili adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8d87-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="d8d87-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d8d87-117">-PassThru</span></span>
<span data-ttu-id="d8d87-118">İşlem başarılı olursa $True döndürür; Aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="d8d87-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="d8d87-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d8d87-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8d87-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8d87-120">-Profile</span></span>
<span data-ttu-id="d8d87-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8d87-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d8d87-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d8d87-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8d87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d87-123">CommonParameters</span></span>
<span data-ttu-id="d8d87-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8d87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d87-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d87-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d87-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8d87-126">INPUTS</span></span>

## <span data-ttu-id="d8d87-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8d87-127">OUTPUTS</span></span>

### <span data-ttu-id="d8d87-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8d87-128">System.Boolean</span></span>
<span data-ttu-id="d8d87-129">Bu cmdlet $True veya $False oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d87-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="d8d87-130">İşlem başarılıysa ve *geçiş parametresini belirtirseniz, bu* cmdlet bir $true değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8d87-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="d8d87-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8d87-131">NOTES</span></span>

## <span data-ttu-id="d8d87-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8d87-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8d87-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d87-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d8d87-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d87-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d8d87-135">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d87-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d8d87-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d87-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d8d87-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d87-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


