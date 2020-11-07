---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: d4523dc240c015f4dea29b86e1285a9fce9afbc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751397"
---
# <span data-ttu-id="5a328-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a328-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="5a328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a328-102">SYNOPSIS</span></span>
<span data-ttu-id="5a328-103">Bir hesabın API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5a328-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="5a328-104">Bu tuşlar, Azure Maps 'e sonraki çağrılarda kullanılan kimlik doğrulama mekanizmasıdır.</span><span class="sxs-lookup"><span data-stu-id="5a328-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="5a328-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a328-105">SYNTAX</span></span>

### <span data-ttu-id="5a328-106">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a328-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a328-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="5a328-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a328-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5a328-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a328-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a328-109">DESCRIPTION</span></span>
<span data-ttu-id="5a328-110">Get-AzMapsAccountKey cmdlet 'i, sağlanan Azure haritalar hesabının API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5a328-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="5a328-111">Azure haritalar hesabında iki API anahtarı vardır: birincil ve Ikincil.</span><span class="sxs-lookup"><span data-stu-id="5a328-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="5a328-112">Anahtarlar, Azure haritalar hesabı uç noktasıyla etkileşimi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="5a328-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="5a328-113">Bir anahtarı yeniden oluşturmak için New-AzMapsAccountKey (New-AzMapsAccountKey. MD) kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a328-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="5a328-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a328-114">EXAMPLES</span></span>

### <span data-ttu-id="5a328-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5a328-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="5a328-116">MyResourceGroup kaynak grubundaki MyAccount adlı hesabın anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a328-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="5a328-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5a328-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="5a328-118">Belirtilen Azure haritalar hesabının anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a328-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="5a328-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a328-119">PARAMETERS</span></span>

### <span data-ttu-id="5a328-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a328-120">-DefaultProfile</span></span>
<span data-ttu-id="5a328-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a328-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a328-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a328-122">-InputObject</span></span>
<span data-ttu-id="5a328-123">Get-AzMapsAccount 'dan yöneltilen hesabı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="5a328-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="5a328-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a328-124">-Name</span></span>
<span data-ttu-id="5a328-125">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="5a328-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="5a328-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a328-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a328-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5a328-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="5a328-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5a328-128">-ResourceId</span></span>
<span data-ttu-id="5a328-129">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="5a328-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="5a328-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a328-130">CommonParameters</span></span>
<span data-ttu-id="5a328-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a328-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a328-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a328-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a328-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a328-133">INPUTS</span></span>

### <span data-ttu-id="5a328-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5a328-134">System.String</span></span>

### <span data-ttu-id="5a328-135">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="5a328-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="5a328-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a328-136">OUTPUTS</span></span>

### <span data-ttu-id="5a328-137">Microsoft. Azure. Commands. Map. model. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5a328-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="5a328-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a328-138">NOTES</span></span>

## <span data-ttu-id="5a328-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a328-139">RELATED LINKS</span></span>
