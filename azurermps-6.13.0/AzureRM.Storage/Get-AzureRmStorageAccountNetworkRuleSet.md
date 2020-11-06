---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589991"
---
# <span data-ttu-id="790cb-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="790cb-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="790cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="790cb-102">SYNOPSIS</span></span>
<span data-ttu-id="790cb-103">Depolama hesabının NetWorkRule özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="790cb-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="790cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="790cb-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="790cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="790cb-105">DESCRIPTION</span></span>
<span data-ttu-id="790cb-106">**Get-AzureRmStorageAccountNetworkRuleSet** cmdlet 'i, bir depolama hesabının networkrule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="790cb-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="790cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="790cb-107">EXAMPLES</span></span>

### <span data-ttu-id="790cb-108">Örnek 1: belirtilen depolama hesabının NetworkRule özelliğini al</span><span class="sxs-lookup"><span data-stu-id="790cb-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="790cb-109">Bu komut belirtilen depolama hesabının NetworkRule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="790cb-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="790cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="790cb-110">PARAMETERS</span></span>

### <span data-ttu-id="790cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790cb-111">-DefaultProfile</span></span>
<span data-ttu-id="790cb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="790cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="790cb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="790cb-113">-Name</span></span>
<span data-ttu-id="790cb-114">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="790cb-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="790cb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790cb-115">-ResourceGroupName</span></span>
<span data-ttu-id="790cb-116">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="790cb-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="790cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790cb-117">CommonParameters</span></span>
<span data-ttu-id="790cb-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="790cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790cb-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790cb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790cb-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="790cb-120">INPUTS</span></span>

### <span data-ttu-id="790cb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="790cb-121">System.String</span></span>

## <span data-ttu-id="790cb-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="790cb-122">OUTPUTS</span></span>

### <span data-ttu-id="790cb-123">Microsoft. Azure. Commands. Management. Storage. model. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="790cb-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="790cb-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="790cb-124">NOTES</span></span>

## <span data-ttu-id="790cb-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="790cb-125">RELATED LINKS</span></span>
