---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320366"
---
# <span data-ttu-id="b75e9-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b75e9-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="b75e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b75e9-103">DataShare hesaplarıyla ilgili bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="b75e9-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="b75e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b75e9-104">SYNTAX</span></span>

### <span data-ttu-id="b75e9-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b75e9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b75e9-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b75e9-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b75e9-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b75e9-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b75e9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b75e9-108">DESCRIPTION</span></span>
<span data-ttu-id="b75e9-109">**Get-AzDataShareAccount** cmdlet 'i, bir Azure aboneliği/kaynak grubundaki datashare hesapları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b75e9-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="b75e9-110">Bir hesabın adını belirtirseniz, bu cmdlet bu datshare hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b75e9-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="b75e9-111">Bir ad belirtmezseniz, bu cmdlet, bir Azure aboneliği/kaynak grubundaki tüm veri paylaşımı hesapları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b75e9-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="b75e9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b75e9-112">EXAMPLES</span></span>

### <span data-ttu-id="b75e9-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b75e9-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="b75e9-114">Bu komut, Azure aboneliğindeki tüm veri paylaşımı hesaplarıyla ilgili bilgileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b75e9-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="b75e9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b75e9-115">PARAMETERS</span></span>

### <span data-ttu-id="b75e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75e9-116">-DefaultProfile</span></span>
<span data-ttu-id="b75e9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b75e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b75e9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b75e9-118">-Name</span></span>
<span data-ttu-id="b75e9-119">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="b75e9-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b75e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="b75e9-121">Azure veri paylaşımı hesabının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b75e9-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75e9-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b75e9-122">-ResourceId</span></span>
<span data-ttu-id="b75e9-123">Azure veri paylaşımı hesabının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b75e9-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b75e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75e9-124">CommonParameters</span></span>
<span data-ttu-id="b75e9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b75e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75e9-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b75e9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75e9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b75e9-127">INPUTS</span></span>

### <span data-ttu-id="b75e9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b75e9-128">System.String</span></span>

## <span data-ttu-id="b75e9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b75e9-129">OUTPUTS</span></span>

### <span data-ttu-id="b75e9-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="b75e9-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="b75e9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b75e9-131">NOTES</span></span>

## <span data-ttu-id="b75e9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b75e9-132">RELATED LINKS</span></span>
