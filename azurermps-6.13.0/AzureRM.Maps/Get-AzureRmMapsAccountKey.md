---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590878"
---
# <span data-ttu-id="7c47a-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="7c47a-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="7c47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c47a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c47a-103">Bir hesabın API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7c47a-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="7c47a-104">Bu tuşlar, Azure Maps 'e sonraki çağrılarda kullanılan kimlik doğrulama mekanizmasıdır.</span><span class="sxs-lookup"><span data-stu-id="7c47a-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c47a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c47a-105">SYNTAX</span></span>

### <span data-ttu-id="7c47a-106">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c47a-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c47a-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="7c47a-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c47a-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7c47a-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c47a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c47a-109">DESCRIPTION</span></span>
<span data-ttu-id="7c47a-110">Get-AzureRmMapsAccountKey cmdlet 'i, sağlanan Azure haritalar hesabının API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7c47a-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="7c47a-111">Azure haritalar hesabında iki API anahtarı vardır: birincil ve Ikincil.</span><span class="sxs-lookup"><span data-stu-id="7c47a-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="7c47a-112">Anahtarlar, Azure haritalar hesabı uç noktasıyla etkileşimi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="7c47a-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="7c47a-113">Bir anahtarı yeniden üretmek için New-AzureRmMapsAccountKey kullanın (New-AzureRmMapsAccountKey. MD).</span><span class="sxs-lookup"><span data-stu-id="7c47a-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="7c47a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c47a-114">EXAMPLES</span></span>

### <span data-ttu-id="7c47a-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7c47a-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7c47a-116">MyResourceGroup kaynak grubundaki MyAccount adlı hesabın anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c47a-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7c47a-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7c47a-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7c47a-118">Belirtilen Azure haritalar hesabının anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c47a-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="7c47a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c47a-119">PARAMETERS</span></span>

### <span data-ttu-id="7c47a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c47a-120">-DefaultProfile</span></span>
<span data-ttu-id="7c47a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c47a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c47a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c47a-122">-InputObject</span></span>
<span data-ttu-id="7c47a-123">Get-AzureRmMapsAccount 'dan yöneltilen hesabı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="7c47a-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c47a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c47a-124">-Name</span></span>
<span data-ttu-id="7c47a-125">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="7c47a-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c47a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c47a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c47a-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7c47a-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c47a-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7c47a-128">-ResourceId</span></span>
<span data-ttu-id="7c47a-129">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="7c47a-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c47a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c47a-130">CommonParameters</span></span>
<span data-ttu-id="7c47a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c47a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c47a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c47a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c47a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c47a-133">INPUTS</span></span>

### <span data-ttu-id="7c47a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7c47a-134">System.String</span></span>

### <span data-ttu-id="7c47a-135">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="7c47a-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="7c47a-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c47a-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7c47a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c47a-137">OUTPUTS</span></span>

### <span data-ttu-id="7c47a-138">Microsoft. Azure. Commands. Map. model. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7c47a-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="7c47a-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c47a-139">NOTES</span></span>

## <span data-ttu-id="7c47a-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c47a-140">RELATED LINKS</span></span>
