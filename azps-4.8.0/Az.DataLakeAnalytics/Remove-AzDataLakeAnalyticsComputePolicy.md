---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109697"
---
# <span data-ttu-id="fb3d2-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fb3d2-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fb3d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3d2-103">Belirtilen Azure Data Lake Analytics COMPUTE ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="fb3d2-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="fb3d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb3d2-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3d2-106">**Remove-AzDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="fb3d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3d2-108">Örnek 1: işlem ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb3d2-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="fb3d2-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="fb3d2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb3d2-110">PARAMETERS</span></span>

### <span data-ttu-id="fb3d2-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="fb3d2-111">-Account</span></span>
<span data-ttu-id="fb3d2-112">İşlem ilkesinin kaldırılacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3d2-113">-DefaultProfile</span></span>
<span data-ttu-id="fb3d2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fb3d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb3d2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb3d2-115">-Name</span></span>
<span data-ttu-id="fb3d2-116">Kaldırılacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d2-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb3d2-117">-PassThru</span></span>
<span data-ttu-id="fb3d2-118">Başarılı bir şekilde silme işlemi</span><span class="sxs-lookup"><span data-stu-id="fb3d2-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="fb3d2-120">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fb3d2-121">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d2-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb3d2-122">-Confirm</span></span>
<span data-ttu-id="fb3d2-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3d2-124">-WhatIf</span></span>
<span data-ttu-id="fb3d2-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3d2-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3d2-127">CommonParameters</span></span>
<span data-ttu-id="fb3d2-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb3d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3d2-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3d2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3d2-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb3d2-130">INPUTS</span></span>

### <span data-ttu-id="fb3d2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3d2-131">System.String</span></span>

## <span data-ttu-id="fb3d2-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb3d2-132">OUTPUTS</span></span>

### <span data-ttu-id="fb3d2-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb3d2-133">System.Boolean</span></span>

## <span data-ttu-id="fb3d2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb3d2-134">NOTES</span></span>

## <span data-ttu-id="fb3d2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb3d2-135">RELATED LINKS</span></span>
