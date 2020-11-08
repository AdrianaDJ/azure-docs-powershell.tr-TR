---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105976"
---
# <span data-ttu-id="1a454-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a454-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="1a454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a454-102">SYNOPSIS</span></span>
<span data-ttu-id="1a454-103">Site kurtarma 'da site kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a454-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="1a454-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a454-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a454-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a454-105">DESCRIPTION</span></span>
<span data-ttu-id="1a454-106">**New-AzureSiteRecoveryRecoveryPlan** cmdlet 'ı Azure Site Recovery 'de bir kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a454-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="1a454-107">Kurtarma planı bir gruptaki sanal makineleri, yük devretme ve kurtarma amacıyla alır.</span><span class="sxs-lookup"><span data-stu-id="1a454-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="1a454-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a454-108">EXAMPLES</span></span>

### <span data-ttu-id="1a454-109">Örnek 1: site kurtarma kasasına kurtarma planı ekleme</span><span class="sxs-lookup"><span data-stu-id="1a454-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="1a454-110">Bu komut RecoveryPlan.xml adlı kurtarma planını Azure Site Recovery kasasına ekler.</span><span class="sxs-lookup"><span data-stu-id="1a454-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="1a454-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a454-111">PARAMETERS</span></span>

### <span data-ttu-id="1a454-112">-Dosya</span><span class="sxs-lookup"><span data-stu-id="1a454-112">-File</span></span>
<span data-ttu-id="1a454-113">Kurtarma planı dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a454-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="1a454-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a454-114">-Profile</span></span>
<span data-ttu-id="1a454-115">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a454-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a454-116">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1a454-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a454-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1a454-117">-WaitForCompletion</span></span>
<span data-ttu-id="1a454-118">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a454-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="1a454-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a454-119">CommonParameters</span></span>
<span data-ttu-id="1a454-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a454-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a454-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a454-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a454-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a454-122">INPUTS</span></span>

## <span data-ttu-id="1a454-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a454-123">OUTPUTS</span></span>

## <span data-ttu-id="1a454-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a454-124">NOTES</span></span>

## <span data-ttu-id="1a454-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a454-125">RELATED LINKS</span></span>

[<span data-ttu-id="1a454-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a454-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="1a454-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a454-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="1a454-128">Güncelleştirme-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a454-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


