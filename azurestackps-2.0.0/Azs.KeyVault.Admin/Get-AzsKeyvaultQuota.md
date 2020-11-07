---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936001"
---
# <span data-ttu-id="cea4e-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="cea4e-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="cea4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea4e-102">SYNOPSIS</span></span>
<span data-ttu-id="cea4e-103">Bir konumdaki Anahtar Kasası için tüm kota nesnelerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="cea4e-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="cea4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cea4e-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cea4e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cea4e-105">DESCRIPTION</span></span>
<span data-ttu-id="cea4e-106">Bir konumdaki Anahtar Kasası için tüm kota nesnelerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="cea4e-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="cea4e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cea4e-107">EXAMPLES</span></span>

### <span data-ttu-id="cea4e-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="cea4e-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="cea4e-109">Bir konumdaki Anahtar Kasası için tüm kota nesnelerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="cea4e-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="cea4e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cea4e-110">PARAMETERS</span></span>

### <span data-ttu-id="cea4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea4e-111">-DefaultProfile</span></span>
<span data-ttu-id="cea4e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cea4e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cea4e-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="cea4e-113">-Location</span></span>
<span data-ttu-id="cea4e-114">Kotanın konumu.</span><span class="sxs-lookup"><span data-stu-id="cea4e-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cea4e-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cea4e-115">-SubscriptionId</span></span>
<span data-ttu-id="cea4e-116">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cea4e-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cea4e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea4e-117">CommonParameters</span></span>
<span data-ttu-id="cea4e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cea4e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea4e-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cea4e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea4e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cea4e-120">INPUTS</span></span>

## <span data-ttu-id="cea4e-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cea4e-121">OUTPUTS</span></span>

### <span data-ttu-id="cea4e-122">Microsoft. Azure. PowerShell. cmdlet. KeyVaultAdmin. modeller. Api20170201Preview. ıquota</span><span class="sxs-lookup"><span data-stu-id="cea4e-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="cea4e-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cea4e-123">NOTES</span></span>

## <span data-ttu-id="cea4e-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cea4e-124">RELATED LINKS</span></span>

