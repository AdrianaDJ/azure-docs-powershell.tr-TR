---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106092"
---
# <span data-ttu-id="8bd7e-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8bd7e-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="8bd7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd7e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd7e-103">Traffic Manager profilinden uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="8bd7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bd7e-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8bd7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bd7e-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd7e-106">**Remove-AzureTrafficManagerEndpoint** cmdlet 'ı Microsoft Azure Traffic Manager profilinden bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8bd7e-107">Uç noktayı kaldırdıktan sonra, Pipeline işlecini kullanarak sonucu **set-AzureTrafficManagerProfile** cmdlet 'ine geçirin.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8bd7e-108">Bu cmdlet değişikliklerinizi kaydetmek için Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="8bd7e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bd7e-109">EXAMPLES</span></span>

### <span data-ttu-id="8bd7e-110">Örnek 1: profilden uç noktayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8bd7e-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="8bd7e-111">İlk komut, ContosoProfile adlı profili almak için **Get-AzureTrafficManagerProfile** cmdlet 'ini kullanır ve ardından $TrafficManagerProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="8bd7e-112">İkinci komut $TrafficManagerProfile depolanan Traffic Manager profilinden etki alanı adı Contoso02App.cloudapp.net olan bir uç noktayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="8bd7e-113">Komut, Azure 'a bağlanarak değişikliklerinizi kaydetmek için profil nesnesini **set-AzureTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="8bd7e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bd7e-114">PARAMETERS</span></span>

### <span data-ttu-id="8bd7e-115">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="8bd7e-115">-DomainName</span></span>
<span data-ttu-id="8bd7e-116">Kaldırılacak uç noktasının etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd7e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8bd7e-117">-Force</span></span>
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

### <span data-ttu-id="8bd7e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="8bd7e-118">-Profile</span></span>
<span data-ttu-id="8bd7e-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8bd7e-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8bd7e-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8bd7e-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="8bd7e-122">Uç noktanın kaldırılacağı Traffic Manager profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd7e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd7e-123">CommonParameters</span></span>
<span data-ttu-id="8bd7e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd7e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd7e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd7e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bd7e-126">INPUTS</span></span>

## <span data-ttu-id="8bd7e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bd7e-127">OUTPUTS</span></span>

### <span data-ttu-id="8bd7e-128">Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition</span><span class="sxs-lookup"><span data-stu-id="8bd7e-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="8bd7e-129">Bu cmdlet, güncelleştirilmiş profil hakkında bilgi içeren bir Traffic Manager profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bd7e-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="8bd7e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bd7e-130">NOTES</span></span>

## <span data-ttu-id="8bd7e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bd7e-131">RELATED LINKS</span></span>

[<span data-ttu-id="8bd7e-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8bd7e-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="8bd7e-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8bd7e-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="8bd7e-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8bd7e-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="8bd7e-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8bd7e-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


