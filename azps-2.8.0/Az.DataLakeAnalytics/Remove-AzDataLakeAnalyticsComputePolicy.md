---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: deafb0cb68ab58997df83bc0280b50a4cc4a0de0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752381"
---
# <span data-ttu-id="fc697-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fc697-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fc697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc697-102">SYNOPSIS</span></span>
<span data-ttu-id="fc697-103">Belirtilen Azure Data Lake Analytics COMPUTE ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="fc697-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="fc697-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc697-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc697-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc697-105">DESCRIPTION</span></span>
<span data-ttu-id="fc697-106">**Remove-AzDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc697-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="fc697-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc697-107">EXAMPLES</span></span>

### <span data-ttu-id="fc697-108">Örnek 1: işlem ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc697-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="fc697-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc697-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="fc697-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc697-110">PARAMETERS</span></span>

### <span data-ttu-id="fc697-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="fc697-111">-Account</span></span>
<span data-ttu-id="fc697-112">İşlem ilkesinin kaldırılacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="fc697-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="fc697-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc697-113">-DefaultProfile</span></span>
<span data-ttu-id="fc697-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc697-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc697-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc697-115">-Name</span></span>
<span data-ttu-id="fc697-116">Kaldırılacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="fc697-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="fc697-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc697-117">-PassThru</span></span>
<span data-ttu-id="fc697-118">Başarılı bir şekilde silme işlemi</span><span class="sxs-lookup"><span data-stu-id="fc697-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="fc697-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc697-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc697-120">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fc697-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fc697-121">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="fc697-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="fc697-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc697-122">-Confirm</span></span>
<span data-ttu-id="fc697-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc697-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc697-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc697-124">-WhatIf</span></span>
<span data-ttu-id="fc697-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc697-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc697-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc697-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc697-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc697-127">CommonParameters</span></span>
<span data-ttu-id="fc697-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc697-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc697-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc697-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc697-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc697-130">INPUTS</span></span>

### <span data-ttu-id="fc697-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fc697-131">System.String</span></span>

## <span data-ttu-id="fc697-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc697-132">OUTPUTS</span></span>

### <span data-ttu-id="fc697-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc697-133">System.Boolean</span></span>

## <span data-ttu-id="fc697-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc697-134">NOTES</span></span>

## <span data-ttu-id="fc697-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc697-135">RELATED LINKS</span></span>
