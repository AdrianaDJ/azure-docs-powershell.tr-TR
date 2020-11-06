---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590875"
---
# <span data-ttu-id="65b66-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="65b66-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="65b66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b66-102">SYNOPSIS</span></span>
<span data-ttu-id="65b66-103">Hesap anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65b66-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65b66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65b66-104">SYNTAX</span></span>

### <span data-ttu-id="65b66-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65b66-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b66-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="65b66-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b66-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="65b66-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b66-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="65b66-108">DESCRIPTION</span></span>
<span data-ttu-id="65b66-109">New-AzureRmMapsAccountKey cmdlet 'i, Azure haritalar hesabı için bir API anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65b66-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="65b66-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65b66-110">EXAMPLES</span></span>

### <span data-ttu-id="65b66-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65b66-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="65b66-112">MyResourceGroup kaynak grubundaki MyAccount hesabı için birincil API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65b66-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="65b66-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="65b66-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="65b66-114">Belirtilen Azure haritalar hesabının Ikincil API anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65b66-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="65b66-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65b66-115">PARAMETERS</span></span>

### <span data-ttu-id="65b66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b66-116">-DefaultProfile</span></span>
<span data-ttu-id="65b66-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65b66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b66-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65b66-118">-InputObject</span></span>
<span data-ttu-id="65b66-119">Get-AzureRmMapsAccount 'dan yöneltilen hesabı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="65b66-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="65b66-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="65b66-120">-KeyName</span></span>
<span data-ttu-id="65b66-121">Harita hesap anahtarı.</span><span class="sxs-lookup"><span data-stu-id="65b66-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b66-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="65b66-122">-Name</span></span>
<span data-ttu-id="65b66-123">Harita hesap adı.</span><span class="sxs-lookup"><span data-stu-id="65b66-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="65b66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b66-124">-ResourceGroupName</span></span>
<span data-ttu-id="65b66-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="65b66-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="65b66-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65b66-126">-ResourceId</span></span>
<span data-ttu-id="65b66-127">Hesap RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="65b66-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="65b66-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="65b66-128">-Confirm</span></span>
<span data-ttu-id="65b66-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65b66-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b66-130">-WhatIf</span></span>
<span data-ttu-id="65b66-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65b66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b66-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65b66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b66-133">CommonParameters</span></span>
<span data-ttu-id="65b66-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65b66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b66-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b66-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b66-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65b66-136">INPUTS</span></span>

### <span data-ttu-id="65b66-137">System. String</span><span class="sxs-lookup"><span data-stu-id="65b66-137">System.String</span></span>

### <span data-ttu-id="65b66-138">Microsoft. Azure. Commands. Map. model. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="65b66-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="65b66-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65b66-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="65b66-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65b66-140">OUTPUTS</span></span>

### <span data-ttu-id="65b66-141">Microsoft. Azure. Management. maps. modeller. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="65b66-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="65b66-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65b66-142">NOTES</span></span>

## <span data-ttu-id="65b66-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65b66-143">RELATED LINKS</span></span>
