---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 5b269eef98072a7daaaf21aa0160167bb714c77a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758681"
---
# <span data-ttu-id="6d576-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d576-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="6d576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d576-102">SYNOPSIS</span></span>
<span data-ttu-id="6d576-103">Depolama hesabının NetWorkRule özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="6d576-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="6d576-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d576-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d576-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d576-105">DESCRIPTION</span></span>
<span data-ttu-id="6d576-106">**Get-AzStorageAccountNetworkRuleSet** cmdlet 'ı bir depolama hesabının networkrule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="6d576-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="6d576-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d576-107">EXAMPLES</span></span>

### <span data-ttu-id="6d576-108">Örnek 1: belirtilen depolama hesabının NetworkRule özelliğini al</span><span class="sxs-lookup"><span data-stu-id="6d576-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="6d576-109">Bu komut belirtilen depolama hesabının NetworkRule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="6d576-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="6d576-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d576-110">PARAMETERS</span></span>

### <span data-ttu-id="6d576-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d576-111">-DefaultProfile</span></span>
<span data-ttu-id="6d576-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d576-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d576-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d576-113">-Name</span></span>
<span data-ttu-id="6d576-114">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d576-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="6d576-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d576-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d576-116">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d576-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="6d576-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d576-117">CommonParameters</span></span>
<span data-ttu-id="6d576-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d576-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d576-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d576-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d576-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d576-120">INPUTS</span></span>

### <span data-ttu-id="6d576-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6d576-121">System.String</span></span>

## <span data-ttu-id="6d576-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d576-122">OUTPUTS</span></span>

### <span data-ttu-id="6d576-123">Microsoft. Azure. Commands. Management. Storage. model. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d576-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6d576-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d576-124">NOTES</span></span>

## <span data-ttu-id="6d576-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d576-125">RELATED LINKS</span></span>
