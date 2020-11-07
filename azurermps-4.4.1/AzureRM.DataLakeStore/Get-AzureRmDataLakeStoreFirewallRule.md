---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763756"
---
# <span data-ttu-id="681b2-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="681b2-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="681b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="681b2-102">SYNOPSIS</span></span>
<span data-ttu-id="681b2-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="681b2-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="681b2-104">Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="681b2-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="681b2-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="681b2-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="681b2-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="681b2-106">DESCRIPTION</span></span>
<span data-ttu-id="681b2-107">Get-AzureRmDataLakeStoreFirewallRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="681b2-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="681b2-108">Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="681b2-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="681b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="681b2-109">EXAMPLES</span></span>

### <span data-ttu-id="681b2-110">Örnek 1: belirli bir güvenlik duvarı kuralını alma</span><span class="sxs-lookup"><span data-stu-id="681b2-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="681b2-111">"Benimfirewallrule" adlı güvenlik duvarı kuralını "ContosoADL" hesabından döndürür</span><span class="sxs-lookup"><span data-stu-id="681b2-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="681b2-112">Örnek 2: bir hesaptaki tüm güvenlik duvarı kurallarını listeleme</span><span class="sxs-lookup"><span data-stu-id="681b2-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="681b2-113">"ContosoADL" hesabındaki tüm güvenlik duvarı kurallarını döndürür</span><span class="sxs-lookup"><span data-stu-id="681b2-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="681b2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="681b2-114">PARAMETERS</span></span>

### <span data-ttu-id="681b2-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="681b2-115">-Account</span></span>
<span data-ttu-id="681b2-116">Güvenlik duvarı kuralının alınacağı veri Lake Store hesabı.</span><span class="sxs-lookup"><span data-stu-id="681b2-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="681b2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="681b2-117">-Name</span></span>
<span data-ttu-id="681b2-118">Alınacak güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="681b2-118">The name of the firewall rule to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="681b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="681b2-120">Belirtilen hesabın belirtilen güvenlik duvarı kuralını almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="681b2-120">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="681b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681b2-121">-DefaultProfile</span></span>
<span data-ttu-id="681b2-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="681b2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="681b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681b2-123">CommonParameters</span></span>
<span data-ttu-id="681b2-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="681b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681b2-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="681b2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681b2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="681b2-126">INPUTS</span></span>

## <span data-ttu-id="681b2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="681b2-127">OUTPUTS</span></span>

### <span data-ttu-id="681b2-128">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="681b2-128">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="681b2-129">Belirtilen güvenlik duvarı kuralı</span><span class="sxs-lookup"><span data-stu-id="681b2-129">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="681b2-130">'Te<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="681b2-130">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="681b2-131">Belirtilen hesaptaki Güvenlik Duvarı kurallarının listesi.</span><span class="sxs-lookup"><span data-stu-id="681b2-131">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="681b2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="681b2-132">NOTES</span></span>

## <span data-ttu-id="681b2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="681b2-133">RELATED LINKS</span></span>

