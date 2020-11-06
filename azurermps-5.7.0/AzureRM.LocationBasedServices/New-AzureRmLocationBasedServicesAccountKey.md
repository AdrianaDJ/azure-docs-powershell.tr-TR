---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 7116cd4c5da2dd897af4e6540593a5e5458e4eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589760"
---
# <span data-ttu-id="29693-101">New-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="29693-101">New-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="29693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29693-102">SYNOPSIS</span></span>
<span data-ttu-id="29693-103">Hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29693-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29693-104">SYNTAX</span></span>

### <span data-ttu-id="29693-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29693-105">NameParameterSet (Default)</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29693-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="29693-106">InputObjectParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29693-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="29693-107">ResourceIdParameterSet</span></span>
```
New-AzureRmLocationBasedServicesAccountKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29693-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="29693-108">DESCRIPTION</span></span>
<span data-ttu-id="29693-109">**Yeni-Azurermlocationbasevseçservicesaccountkey** cmdlet 'ı konum tabanlı hizmetler hesabı IÇIN bir API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29693-109">The **New-AzureRmLocationBasedServicesAccountKey** cmdlet regenerates an API key for a Location Based Services account.</span></span>

## <span data-ttu-id="29693-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29693-110">EXAMPLES</span></span>

### <span data-ttu-id="29693-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29693-111">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="29693-112">MyResourceGroup kaynak grubundaki MyAccount hesabı için birincil API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29693-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="29693-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="29693-113">Example 2</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="29693-114">Belirtilen konum tabanlı hizmetler hesabının Ikincil API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29693-114">Regenerates the Secondary API Key for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="29693-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29693-115">PARAMETERS</span></span>

### <span data-ttu-id="29693-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29693-116">-DefaultProfile</span></span>
<span data-ttu-id="29693-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29693-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29693-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29693-118">-InputObject</span></span>
<span data-ttu-id="29693-119">[Get-Azurermlocationbasevseçservicesaccount](Get-AzureRmLocationBasedServicesAccount.md)'dan yöneltilen konum tabanlı hizmetler hesabı.</span><span class="sxs-lookup"><span data-stu-id="29693-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29693-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="29693-120">-KeyName</span></span>
<span data-ttu-id="29693-121">Konum tabanlı hizmetler hesap anahtarı.</span><span class="sxs-lookup"><span data-stu-id="29693-121">Location Based Services Account Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29693-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="29693-122">-Name</span></span>
<span data-ttu-id="29693-123">Konum tabanlı hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="29693-123">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29693-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29693-124">-ResourceGroupName</span></span>
<span data-ttu-id="29693-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="29693-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29693-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="29693-126">-ResourceId</span></span>
<span data-ttu-id="29693-127">Konum temelli hizmetler hesabı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="29693-127">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29693-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="29693-128">-Confirm</span></span>
<span data-ttu-id="29693-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29693-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29693-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29693-130">-WhatIf</span></span>
<span data-ttu-id="29693-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29693-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29693-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29693-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29693-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29693-133">CommonParameters</span></span>
<span data-ttu-id="29693-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29693-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29693-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29693-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29693-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29693-136">INPUTS</span></span>

### <span data-ttu-id="29693-137">System. String</span><span class="sxs-lookup"><span data-stu-id="29693-137">System.String</span></span>
<span data-ttu-id="29693-138">Microsoft. Azure. Commands. Locationbasevseçservices. NewAzureLocationBasedServicesAccountKeyCommand + KeyNameType</span><span class="sxs-lookup"><span data-stu-id="29693-138">Microsoft.Azure.Commands.LocationBasedServices.NewAzureLocationBasedServicesAccountKeyCommand+KeyNameType</span></span>

## <span data-ttu-id="29693-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29693-139">OUTPUTS</span></span>

### <span data-ttu-id="29693-140">Microsoft. Azure. Management. Locationbasevseçservice. model. Locationbasevseçservicesaccountkeys</span><span class="sxs-lookup"><span data-stu-id="29693-140">Microsoft.Azure.Management.LocationBasedServices.Models.LocationBasedServicesAccountKeys</span></span>

## <span data-ttu-id="29693-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29693-141">NOTES</span></span>

## <span data-ttu-id="29693-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29693-142">RELATED LINKS</span></span>
