---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573233"
---
# <span data-ttu-id="3a5f4-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3a5f4-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="3a5f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5f4-103">Site kurtarma 'da kurtarma planını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a5f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a5f4-104">SYNTAX</span></span>

### <span data-ttu-id="3a5f4-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a5f4-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a5f4-106">Byrpfıle</span><span class="sxs-lookup"><span data-stu-id="3a5f4-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a5f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a5f4-107">DESCRIPTION</span></span>
<span data-ttu-id="3a5f4-108">**Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet 'ı Azure Site Recovery 'de bir kurtarma planını güncelleştirir ve sonra yayımlar.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="3a5f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a5f4-109">EXAMPLES</span></span>

### <span data-ttu-id="3a5f4-110">Örnek 1: kurtarma planını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3a5f4-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="3a5f4-111">Bu komut belirtilen kurtarma planını güncelleştirir ve yayımlar.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="3a5f4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a5f4-112">PARAMETERS</span></span>

### <span data-ttu-id="3a5f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5f4-113">-DefaultProfile</span></span>
<span data-ttu-id="3a5f4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a5f4-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="3a5f4-115">-Path</span></span>
<span data-ttu-id="3a5f4-116">Bu cmdlet 'in güncelleştirdiği kurtarma planının kurtarma planı dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f4-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3a5f4-117">-RecoveryPlan</span></span>
<span data-ttu-id="3a5f4-118">Bu cmdlet 'in güncelleştirdiği kurtarma planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5f4-119">CommonParameters</span></span>
<span data-ttu-id="3a5f4-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a5f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5f4-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5f4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5f4-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a5f4-122">INPUTS</span></span>

### <span data-ttu-id="3a5f4-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3a5f4-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="3a5f4-124">' RecoveryPlan ' parametresi ardışık düzenin ' ASRRecoveryPlan ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a5f4-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="3a5f4-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a5f4-125">OUTPUTS</span></span>

## <span data-ttu-id="3a5f4-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a5f4-126">NOTES</span></span>

## <span data-ttu-id="3a5f4-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a5f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="3a5f4-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3a5f4-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="3a5f4-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3a5f4-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="3a5f4-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3a5f4-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


