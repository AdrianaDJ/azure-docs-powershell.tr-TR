---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106014"
---
# <span data-ttu-id="f10bb-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10bb-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="f10bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f10bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f10bb-103">Site kurtarma 'da kurtarma planını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f10bb-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="f10bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f10bb-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f10bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f10bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f10bb-106">**Update-AzureSiteRecoveryRecoveryPlan** cmdlet 'ı Azure Site Recovery 'de bir kurtarma planını güncelleştirir ve sonra yayımlar.</span><span class="sxs-lookup"><span data-stu-id="f10bb-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="f10bb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f10bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f10bb-108">Örnek 1: kurtarma planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f10bb-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="f10bb-109">Bu komut belirtilen kurtarma planını güncelleştirir ve yayımlar.</span><span class="sxs-lookup"><span data-stu-id="f10bb-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="f10bb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f10bb-110">PARAMETERS</span></span>

### <span data-ttu-id="f10bb-111">-Dosya</span><span class="sxs-lookup"><span data-stu-id="f10bb-111">-File</span></span>
<span data-ttu-id="f10bb-112">Bu cmdlet 'in güncelleştirdiği kurtarma planının kurtarma planı dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f10bb-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f10bb-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="f10bb-113">-Profile</span></span>
<span data-ttu-id="f10bb-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f10bb-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f10bb-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f10bb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f10bb-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f10bb-116">-WaitForCompletion</span></span>
<span data-ttu-id="f10bb-117">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f10bb-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f10bb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10bb-118">CommonParameters</span></span>
<span data-ttu-id="f10bb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f10bb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10bb-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10bb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10bb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f10bb-121">INPUTS</span></span>

## <span data-ttu-id="f10bb-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f10bb-122">OUTPUTS</span></span>

## <span data-ttu-id="f10bb-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f10bb-123">NOTES</span></span>

## <span data-ttu-id="f10bb-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f10bb-124">RELATED LINKS</span></span>

[<span data-ttu-id="f10bb-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10bb-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f10bb-126">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10bb-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f10bb-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f10bb-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


