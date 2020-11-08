---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276868"
---
# <span data-ttu-id="f0c28-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="f0c28-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="f0c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c28-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c28-103">Bir abonelikteki veya Resource grubundaki tüm kaynaklar için ilke uyumluluğu değerlendirmesini tetikler.</span><span class="sxs-lookup"><span data-stu-id="f0c28-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="f0c28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0c28-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0c28-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c28-106">**Start-Azpolicykarmaşıs,** cmdlet 'i bir abonelik veya kaynak grubu için ilke uyumluluk değerlendirmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="f0c28-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="f0c28-107">Bu kapsamdaki tüm kaynakların uyumluluk durumu tüm atanmış ilkelere göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="f0c28-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="f0c28-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0c28-108">EXAMPLES</span></span>

### <span data-ttu-id="f0c28-109">Örnek 1: abonelik kapsamında uyumluluk taraması başlatma</span><span class="sxs-lookup"><span data-stu-id="f0c28-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="f0c28-110">Bu komut etkin abonelik için ilke uyumluluk değerlendirmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="f0c28-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="f0c28-111">Örnek 2: kaynak grup kapsamında uyumluluk taraması başlatma</span><span class="sxs-lookup"><span data-stu-id="f0c28-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="f0c28-112">Bu komut, etkin abonelikteki "Benimrg" kaynak grubu için ilke uyumluluk değerlendirmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="f0c28-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="f0c28-113">Örnek 3: uyumluluk taraması başlatın ve arka planda tamamlamasını bekleyin</span><span class="sxs-lookup"><span data-stu-id="f0c28-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="f0c28-114">Bu komut etkin abonelik için ilke uyumluluk değerlendirmesi başlatır.</span><span class="sxs-lookup"><span data-stu-id="f0c28-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="f0c28-115">Taramanın tamamlanması bekleyecek.</span><span class="sxs-lookup"><span data-stu-id="f0c28-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="f0c28-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0c28-116">PARAMETERS</span></span>

### <span data-ttu-id="f0c28-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="f0c28-117">-AsJob</span></span>
<span data-ttu-id="f0c28-118">Arka planda cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f0c28-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f0c28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c28-119">-DefaultProfile</span></span>
<span data-ttu-id="f0c28-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0c28-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c28-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f0c28-121">-PassThru</span></span>
<span data-ttu-id="f0c28-122">Komut başarılı bir şekilde tamamlandığında doğru döner.</span><span class="sxs-lookup"><span data-stu-id="f0c28-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="f0c28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c28-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0c28-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f0c28-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c28-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0c28-125">-Confirm</span></span>
<span data-ttu-id="f0c28-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0c28-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c28-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c28-127">-WhatIf</span></span>
<span data-ttu-id="f0c28-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0c28-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c28-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0c28-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c28-130">CommonParameters</span></span>
<span data-ttu-id="f0c28-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0c28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c28-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0c28-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c28-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0c28-133">INPUTS</span></span>

### <span data-ttu-id="f0c28-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c28-134">System.String</span></span>

## <span data-ttu-id="f0c28-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0c28-135">OUTPUTS</span></span>

### <span data-ttu-id="f0c28-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0c28-136">System.Boolean</span></span>

## <span data-ttu-id="f0c28-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0c28-137">NOTES</span></span>

## <span data-ttu-id="f0c28-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0c28-138">RELATED LINKS</span></span>
