---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763961"
---
# <span data-ttu-id="b2c3c-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c3c-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="b2c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c3c-103">Site kurtarma planını site kurtarmadan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2c3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2c3c-104">SYNTAX</span></span>

### <span data-ttu-id="b2c3c-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2c3c-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2c3c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b2c3c-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2c3c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2c3c-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c3c-108">**Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet 'ı geçerli Azure Site Recovery 'den bir site kurtarma planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="b2c3c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2c3c-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c3c-110">Örnek 1: kurtarma planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b2c3c-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="b2c3c-111">İlk komut Get-AzureRmSiteRecoveryRecoveryPlan cmdlet 'ini kullanarak site kurtarma planını alır ve $RecoveryPlan değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="b2c3c-112">İkinci komut $RecoveryPlan 'da kurtarma planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="b2c3c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2c3c-113">PARAMETERS</span></span>

### <span data-ttu-id="b2c3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c3c-114">-DefaultProfile</span></span>
<span data-ttu-id="b2c3c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c3c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2c3c-116">-Name</span></span>
<span data-ttu-id="b2c3c-117">Bu cmdlet 'in kaldırıldığı kurtarma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-117">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c3c-118">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c3c-118">-RecoveryPlan</span></span>
<span data-ttu-id="b2c3c-119">Bu cmdlet 'in kaldırıldığı kurtarma planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-119">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c3c-120">CommonParameters</span></span>
<span data-ttu-id="b2c3c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2c3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c3c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c3c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c3c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2c3c-123">INPUTS</span></span>

### <span data-ttu-id="b2c3c-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c3c-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="b2c3c-125">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b2c3c-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="b2c3c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2c3c-126">OUTPUTS</span></span>

## <span data-ttu-id="b2c3c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2c3c-127">NOTES</span></span>

## <span data-ttu-id="b2c3c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2c3c-128">RELATED LINKS</span></span>

[<span data-ttu-id="b2c3c-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c3c-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b2c3c-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c3c-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="b2c3c-131">Güncelleştirme-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c3c-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


