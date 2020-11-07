---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939218"
---
# <span data-ttu-id="60114-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="60114-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="60114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60114-102">SYNOPSIS</span></span>
<span data-ttu-id="60114-103">Depolama hesabının NetWorkRule özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="60114-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60114-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60114-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60114-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60114-105">DESCRIPTION</span></span>
<span data-ttu-id="60114-106">**Get-AzureRmStorageAccountNetworkRuleSet** cmdlet 'i, bir depolama hesabının networkrule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="60114-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="60114-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60114-107">EXAMPLES</span></span>

### <span data-ttu-id="60114-108">Örnek 1: belirtilen depolama hesabının NetworkRule özelliğini al</span><span class="sxs-lookup"><span data-stu-id="60114-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="60114-109">Bu komut belirtilen depolama hesabının NetworkRule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="60114-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="60114-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60114-110">PARAMETERS</span></span>

### <span data-ttu-id="60114-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60114-111">-DefaultProfile</span></span>
<span data-ttu-id="60114-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60114-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60114-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="60114-113">-Name</span></span>
<span data-ttu-id="60114-114">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60114-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="60114-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60114-115">-ResourceGroupName</span></span>
<span data-ttu-id="60114-116">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60114-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="60114-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60114-117">CommonParameters</span></span>
<span data-ttu-id="60114-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60114-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60114-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60114-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60114-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60114-120">INPUTS</span></span>

### <span data-ttu-id="60114-121">System. String</span><span class="sxs-lookup"><span data-stu-id="60114-121">System.String</span></span>

## <span data-ttu-id="60114-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60114-122">OUTPUTS</span></span>

### <span data-ttu-id="60114-123">Microsoft. Azure. Commands. Management. Storage. model. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="60114-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="60114-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60114-124">NOTES</span></span>

## <span data-ttu-id="60114-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60114-125">RELATED LINKS</span></span>
