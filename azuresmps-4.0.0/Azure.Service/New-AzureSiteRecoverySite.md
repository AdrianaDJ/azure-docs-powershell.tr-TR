---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105892"
---
# <span data-ttu-id="30ea4-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="30ea4-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="30ea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="30ea4-103">Site kurtarma sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30ea4-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="30ea4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30ea4-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30ea4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="30ea4-106">**New-AzureSiteRecoverySite** cmdlet 'i geçerli kasada bir Azure Site kurtarma sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30ea4-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="30ea4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="30ea4-108">Örnek 1: site kurtarma sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="30ea4-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="30ea4-109">Bu komut, RecoverySite07 adlı bir site kurtarma sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30ea4-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="30ea4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="30ea4-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="30ea4-111">-Name</span></span>
<span data-ttu-id="30ea4-112">Sitenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ea4-112">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="30ea4-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="30ea4-113">-Profile</span></span>
<span data-ttu-id="30ea4-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ea4-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30ea4-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="30ea4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30ea4-116">-Kasa</span><span class="sxs-lookup"><span data-stu-id="30ea4-116">-Vault</span></span>
<span data-ttu-id="30ea4-117">Sitenin oluşturulacağı bir kasa belirtir.</span><span class="sxs-lookup"><span data-stu-id="30ea4-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="30ea4-118">Bir **Asrkasa** nesnesi edinmek için **Get-AzureSiteRecoveryVault** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="30ea4-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ea4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ea4-119">CommonParameters</span></span>
<span data-ttu-id="30ea4-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30ea4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ea4-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ea4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ea4-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30ea4-122">INPUTS</span></span>

## <span data-ttu-id="30ea4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30ea4-123">OUTPUTS</span></span>

## <span data-ttu-id="30ea4-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30ea4-124">NOTES</span></span>

## <span data-ttu-id="30ea4-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30ea4-125">RELATED LINKS</span></span>

[<span data-ttu-id="30ea4-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="30ea4-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="30ea4-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="30ea4-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


