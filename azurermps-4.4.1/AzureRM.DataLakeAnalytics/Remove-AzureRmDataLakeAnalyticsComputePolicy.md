---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593156"
---
# <span data-ttu-id="b243f-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b243f-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b243f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b243f-102">SYNOPSIS</span></span>
<span data-ttu-id="b243f-103">Belirtilen Azure Data Lake Analytics COMPUTE ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="b243f-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b243f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b243f-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b243f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b243f-105">DESCRIPTION</span></span>
<span data-ttu-id="b243f-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** , belirtilen bir Azure Data Lake Analytics COMPUTE ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b243f-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="b243f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b243f-107">EXAMPLES</span></span>

### <span data-ttu-id="b243f-108">Örnek 1: işlem ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b243f-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="b243f-109">Bu komut, ' contosoadla ' hesabında ' myPolicy ' adlı belirtilen hesaplama ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b243f-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="b243f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b243f-110">PARAMETERS</span></span>

### <span data-ttu-id="b243f-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="b243f-111">-Account</span></span>
<span data-ttu-id="b243f-112">İşlem ilkesinin kaldırılacağı hesabın adı.</span><span class="sxs-lookup"><span data-stu-id="b243f-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="b243f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b243f-113">-Name</span></span>
<span data-ttu-id="b243f-114">Kaldırılacak işlem ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="b243f-114">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="b243f-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b243f-115">-PassThru</span></span>
<span data-ttu-id="b243f-116">Başarılı bir şekilde silme işlemi</span><span class="sxs-lookup"><span data-stu-id="b243f-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="b243f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b243f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b243f-118">Hesabınızın bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b243f-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="b243f-119">İsteğe bağlı olarak, sağlanmadıysa bulmaya çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="b243f-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="b243f-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="b243f-120">-Confirm</span></span>
<span data-ttu-id="b243f-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b243f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b243f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b243f-122">-WhatIf</span></span>
<span data-ttu-id="b243f-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b243f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b243f-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b243f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b243f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b243f-125">-DefaultProfile</span></span>
<span data-ttu-id="b243f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b243f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b243f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b243f-127">CommonParameters</span></span>
<span data-ttu-id="b243f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b243f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b243f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b243f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b243f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b243f-130">INPUTS</span></span>

### <span data-ttu-id="b243f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b243f-131">System.String</span></span>

## <span data-ttu-id="b243f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b243f-132">OUTPUTS</span></span>

### <span data-ttu-id="b243f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b243f-133">System.Boolean</span></span>

## <span data-ttu-id="b243f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b243f-134">NOTES</span></span>

## <span data-ttu-id="b243f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b243f-135">RELATED LINKS</span></span>

