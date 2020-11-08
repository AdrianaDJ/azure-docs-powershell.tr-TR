---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109399"
---
# <span data-ttu-id="75d36-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="75d36-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="75d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d36-102">SYNOPSIS</span></span>
<span data-ttu-id="75d36-103">PeerAsn için bellek içi kişi ayrıntısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75d36-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="75d36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75d36-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d36-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75d36-105">DESCRIPTION</span></span>
<span data-ttu-id="75d36-106">Bellekte PeerAsn iletişim ayrıntılarını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="75d36-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="75d36-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75d36-107">EXAMPLES</span></span>

### <span data-ttu-id="75d36-108">Kişi ayrıntısı oluşturma ve PeerAsn 'ye ekleme</span><span class="sxs-lookup"><span data-stu-id="75d36-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="75d36-109">Rol ve e-posta gereklidir.</span><span class="sxs-lookup"><span data-stu-id="75d36-109">Role and email are required.</span></span> <span data-ttu-id="75d36-110">Telefon isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="75d36-110">Phone is optional.</span></span> <span data-ttu-id="75d36-111">Telefon +-() veya boşlukları destekler.</span><span class="sxs-lookup"><span data-stu-id="75d36-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="75d36-112">Bir PeerAsn "NOC" türünde en az bir kişi ayrıntısı içermelidir</span><span class="sxs-lookup"><span data-stu-id="75d36-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="75d36-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75d36-113">PARAMETERS</span></span>

### <span data-ttu-id="75d36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d36-114">-DefaultProfile</span></span>
<span data-ttu-id="75d36-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75d36-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d36-116">-E-posta</span><span class="sxs-lookup"><span data-stu-id="75d36-116">-Email</span></span>
<span data-ttu-id="75d36-117">Genellikle ağ Işlemleri merkezi Arrise sorun yaşıyorsanız iletişim kurmak için kullanılan e-posta adresleri</span><span class="sxs-lookup"><span data-stu-id="75d36-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d36-118">-Telefon</span><span class="sxs-lookup"><span data-stu-id="75d36-118">-Phone</span></span>
<span data-ttu-id="75d36-119">Genellikle ağ Işlemleri merkezi Arrise sorun yaşıyorsanız iletişim kurmak için kullanılan telefon</span><span class="sxs-lookup"><span data-stu-id="75d36-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d36-120">-Role</span><span class="sxs-lookup"><span data-stu-id="75d36-120">-Role</span></span>
<span data-ttu-id="75d36-121">Kişi bilgilerine en uygun rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="75d36-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="75d36-122">NOC kişisi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="75d36-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d36-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d36-123">CommonParameters</span></span>
<span data-ttu-id="75d36-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75d36-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d36-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75d36-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d36-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75d36-126">INPUTS</span></span>

### <span data-ttu-id="75d36-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="75d36-127">None</span></span>

## <span data-ttu-id="75d36-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75d36-128">OUTPUTS</span></span>

### <span data-ttu-id="75d36-129">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d36-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="75d36-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75d36-130">NOTES</span></span>

## <span data-ttu-id="75d36-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75d36-131">RELATED LINKS</span></span>
