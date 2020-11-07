---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 74c066cd59497603da4f953f35ed16e454e67155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762802"
---
# <span data-ttu-id="76603-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76603-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="76603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76603-102">SYNOPSIS</span></span>
<span data-ttu-id="76603-103">Bir hesabı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="76603-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76603-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76603-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76603-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76603-105">DESCRIPTION</span></span>
<span data-ttu-id="76603-106">**Set-Azurermöğretici Iveservicesaccount** cmdlet 'i, belirtilen öğretici sitif HIZMETLER hesabının SKU veya etiketlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="76603-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="76603-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76603-107">EXAMPLES</span></span>

### <span data-ttu-id="76603-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76603-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="76603-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76603-109">PARAMETERS</span></span>

### <span data-ttu-id="76603-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76603-110">-DefaultProfile</span></span>
<span data-ttu-id="76603-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="76603-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76603-112">-Force</span><span class="sxs-lookup"><span data-stu-id="76603-112">-Force</span></span>
<span data-ttu-id="76603-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="76603-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76603-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="76603-114">-Name</span></span>
<span data-ttu-id="76603-115">Değiştirilecek hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76603-115">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76603-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76603-116">-ResourceGroupName</span></span>
<span data-ttu-id="76603-117">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76603-117">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76603-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76603-118">-SkuName</span></span>
<span data-ttu-id="76603-119">Hesabın STB 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="76603-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="76603-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="76603-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76603-121">F0 (serbest katman)</span><span class="sxs-lookup"><span data-stu-id="76603-121">F0 (free tier)</span></span>
- <span data-ttu-id="76603-122">S0</span><span class="sxs-lookup"><span data-stu-id="76603-122">S0</span></span>
- <span data-ttu-id="76603-123">S1</span><span class="sxs-lookup"><span data-stu-id="76603-123">S1</span></span>
- <span data-ttu-id="76603-124">S2</span><span class="sxs-lookup"><span data-stu-id="76603-124">S2</span></span>
- <span data-ttu-id="76603-125">S3</span><span class="sxs-lookup"><span data-stu-id="76603-125">S3</span></span>
- <span data-ttu-id="76603-126">Modundan</span><span class="sxs-lookup"><span data-stu-id="76603-126">S4</span></span>

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

### <span data-ttu-id="76603-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="76603-127">-Tag</span></span>
<span data-ttu-id="76603-128">Ad/değer çifti olarak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="76603-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76603-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="76603-129">-Confirm</span></span>
<span data-ttu-id="76603-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76603-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76603-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76603-131">-WhatIf</span></span>
<span data-ttu-id="76603-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76603-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76603-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76603-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76603-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76603-134">CommonParameters</span></span>
<span data-ttu-id="76603-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76603-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76603-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76603-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76603-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76603-137">INPUTS</span></span>

### <span data-ttu-id="76603-138">System. String</span><span class="sxs-lookup"><span data-stu-id="76603-138">System.String</span></span>

### <span data-ttu-id="76603-139">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="76603-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="76603-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76603-140">OUTPUTS</span></span>

### <span data-ttu-id="76603-141">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="76603-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="76603-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76603-142">NOTES</span></span>

## <span data-ttu-id="76603-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76603-143">RELATED LINKS</span></span>

[<span data-ttu-id="76603-144">Get-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="76603-144">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="76603-145">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="76603-145">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="76603-146">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="76603-146">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
