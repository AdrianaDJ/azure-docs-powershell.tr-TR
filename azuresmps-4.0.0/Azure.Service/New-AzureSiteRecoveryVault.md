---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105974"
---
# <span data-ttu-id="fa00b-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fa00b-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="fa00b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa00b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa00b-103">Site Recovery Services Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa00b-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="fa00b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa00b-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa00b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa00b-105">DESCRIPTION</span></span>
<span data-ttu-id="fa00b-106">**New-AzureSiteRecoveryVault** cmdlet 'ı bir Azure Site Recovery Services Kasası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa00b-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="fa00b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa00b-107">EXAMPLES</span></span>

### <span data-ttu-id="fa00b-108">Örnek 1: kasa oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa00b-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="fa00b-109">Bu komut, Batı Amerika konumunda Contosokasası adlı bir kasa oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa00b-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="fa00b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa00b-110">PARAMETERS</span></span>

### <span data-ttu-id="fa00b-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="fa00b-111">-Location</span></span>
<span data-ttu-id="fa00b-112">Coğrafi konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa00b-112">Specifies the geographical location.</span></span>

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

### <span data-ttu-id="fa00b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa00b-113">-Name</span></span>
<span data-ttu-id="fa00b-114">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa00b-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="fa00b-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="fa00b-115">-Profile</span></span>
<span data-ttu-id="fa00b-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa00b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa00b-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fa00b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa00b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa00b-118">CommonParameters</span></span>
<span data-ttu-id="fa00b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa00b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa00b-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa00b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa00b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa00b-121">INPUTS</span></span>

## <span data-ttu-id="fa00b-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa00b-122">OUTPUTS</span></span>

## <span data-ttu-id="fa00b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa00b-123">NOTES</span></span>

## <span data-ttu-id="fa00b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa00b-124">RELATED LINKS</span></span>

[<span data-ttu-id="fa00b-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fa00b-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


