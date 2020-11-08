---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096305"
---
# <span data-ttu-id="4f9a9-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4f9a9-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4f9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9a9-103">Belirtilen Azure Data Lake Analytics COMPUTE ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="4f9a9-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="4f9a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f9a9-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f9a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="4f9a9-106">**Remove-AzDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="4f9a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="4f9a9-108">Örnek 1: işlem ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f9a9-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="4f9a9-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="4f9a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="4f9a9-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="4f9a9-111">-Account</span></span>
<span data-ttu-id="4f9a9-112">İşlem ilkesinin kaldırılacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="4f9a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9a9-113">-DefaultProfile</span></span>
<span data-ttu-id="4f9a9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f9a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f9a9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f9a9-115">-Name</span></span>
<span data-ttu-id="4f9a9-116">Kaldırılacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="4f9a9-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f9a9-117">-PassThru</span></span>
<span data-ttu-id="4f9a9-118">Başarılı bir şekilde silme işlemi</span><span class="sxs-lookup"><span data-stu-id="4f9a9-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="4f9a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f9a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f9a9-120">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4f9a9-121">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4f9a9-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f9a9-122">-Confirm</span></span>
<span data-ttu-id="4f9a9-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f9a9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f9a9-124">-WhatIf</span></span>
<span data-ttu-id="4f9a9-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f9a9-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f9a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9a9-127">CommonParameters</span></span>
<span data-ttu-id="4f9a9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f9a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9a9-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f9a9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9a9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f9a9-130">INPUTS</span></span>

### <span data-ttu-id="4f9a9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4f9a9-131">System.String</span></span>

## <span data-ttu-id="4f9a9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f9a9-132">OUTPUTS</span></span>

### <span data-ttu-id="4f9a9-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f9a9-133">System.Boolean</span></span>

## <span data-ttu-id="4f9a9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f9a9-134">NOTES</span></span>

## <span data-ttu-id="4f9a9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f9a9-135">RELATED LINKS</span></span>