---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: e8db3842997a5bd99b970921b31d66bbbc07007a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588943"
---
# <span data-ttu-id="7044e-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7044e-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="7044e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7044e-102">SYNOPSIS</span></span>
<span data-ttu-id="7044e-103">Belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="7044e-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="7044e-104">Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7044e-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7044e-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7044e-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7044e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="7044e-106">DESCRIPTION</span></span>
<span data-ttu-id="7044e-107">Get-AzureRmDataLakeStoreFirewallRule cmdlet 'i belirtilen veri Lake Store 'da belirtilen güvenlik duvarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="7044e-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="7044e-108">Güvenlik duvarı kuralı belirtilmezse, hesabın tüm güvenlik duvarı kurallarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7044e-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="7044e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7044e-109">EXAMPLES</span></span>

### <span data-ttu-id="7044e-110">Örnek 1: belirli bir güvenlik duvarı kuralını alma</span><span class="sxs-lookup"><span data-stu-id="7044e-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="7044e-111">"Benimfirewallrule" adlı güvenlik duvarı kuralını "ContosoADL" hesabından döndürür</span><span class="sxs-lookup"><span data-stu-id="7044e-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="7044e-112">Örnek 2: bir hesaptaki tüm güvenlik duvarı kurallarını listeleme</span><span class="sxs-lookup"><span data-stu-id="7044e-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="7044e-113">"ContosoADL" hesabındaki tüm güvenlik duvarı kurallarını döndürür</span><span class="sxs-lookup"><span data-stu-id="7044e-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="7044e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7044e-114">PARAMETERS</span></span>

### <span data-ttu-id="7044e-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="7044e-115">-Account</span></span>
<span data-ttu-id="7044e-116">Güvenlik duvarı kuralının alınacağı veri Lake Store hesabı.</span><span class="sxs-lookup"><span data-stu-id="7044e-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7044e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7044e-117">-DefaultProfile</span></span>
<span data-ttu-id="7044e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7044e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7044e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7044e-119">-Name</span></span>
<span data-ttu-id="7044e-120">Alınacak güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="7044e-120">The name of the firewall rule to retrieve</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7044e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7044e-121">-ResourceGroupName</span></span>
<span data-ttu-id="7044e-122">Belirtilen hesabın belirtilen güvenlik duvarı kuralını almak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7044e-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7044e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7044e-123">CommonParameters</span></span>
<span data-ttu-id="7044e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7044e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7044e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7044e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7044e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7044e-126">INPUTS</span></span>

### <span data-ttu-id="7044e-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7044e-127">None</span></span>
<span data-ttu-id="7044e-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7044e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7044e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7044e-129">OUTPUTS</span></span>

### <span data-ttu-id="7044e-130">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7044e-130">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="7044e-131">Belirtilen güvenlik duvarı kuralı</span><span class="sxs-lookup"><span data-stu-id="7044e-131">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="7044e-132">'Te<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="7044e-132">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="7044e-133">Belirtilen hesaptaki Güvenlik Duvarı kurallarının listesi.</span><span class="sxs-lookup"><span data-stu-id="7044e-133">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="7044e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7044e-134">NOTES</span></span>

## <span data-ttu-id="7044e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7044e-135">RELATED LINKS</span></span>

