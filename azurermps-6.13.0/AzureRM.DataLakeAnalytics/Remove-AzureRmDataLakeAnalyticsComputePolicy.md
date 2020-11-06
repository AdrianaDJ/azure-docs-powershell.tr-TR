---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: a97c6835144cda227fc07645f087e393cda2b8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588497"
---
# <span data-ttu-id="2019d-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="2019d-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="2019d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2019d-102">SYNOPSIS</span></span>
<span data-ttu-id="2019d-103">Belirtilen Azure Data Lake Analytics COMPUTE ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="2019d-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2019d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2019d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2019d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2019d-105">DESCRIPTION</span></span>
<span data-ttu-id="2019d-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2019d-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="2019d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2019d-107">EXAMPLES</span></span>

### <span data-ttu-id="2019d-108">Örnek 1: işlem ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="2019d-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="2019d-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2019d-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="2019d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2019d-110">PARAMETERS</span></span>

### <span data-ttu-id="2019d-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2019d-111">-Account</span></span>
<span data-ttu-id="2019d-112">İşlem ilkesinin kaldırılacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="2019d-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="2019d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2019d-113">-DefaultProfile</span></span>
<span data-ttu-id="2019d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2019d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2019d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2019d-115">-Name</span></span>
<span data-ttu-id="2019d-116">Kaldırılacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="2019d-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="2019d-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2019d-117">-PassThru</span></span>
<span data-ttu-id="2019d-118">Başarılı bir şekilde silme işlemi</span><span class="sxs-lookup"><span data-stu-id="2019d-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="2019d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2019d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2019d-120">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2019d-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="2019d-121">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="2019d-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="2019d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="2019d-122">-Confirm</span></span>
<span data-ttu-id="2019d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2019d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2019d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2019d-124">-WhatIf</span></span>
<span data-ttu-id="2019d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2019d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2019d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2019d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2019d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2019d-127">CommonParameters</span></span>
<span data-ttu-id="2019d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2019d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2019d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2019d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2019d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2019d-130">INPUTS</span></span>

### <span data-ttu-id="2019d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2019d-131">System.String</span></span>

## <span data-ttu-id="2019d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2019d-132">OUTPUTS</span></span>

### <span data-ttu-id="2019d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2019d-133">System.Boolean</span></span>

## <span data-ttu-id="2019d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2019d-134">NOTES</span></span>

## <span data-ttu-id="2019d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2019d-135">RELATED LINKS</span></span>
