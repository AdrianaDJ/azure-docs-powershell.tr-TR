---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586690"
---
# <span data-ttu-id="d3a83-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d3a83-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="d3a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a83-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a83-103">Günlüğe kaydedilen kategorileri ve zaman grateleri alır.</span><span class="sxs-lookup"><span data-stu-id="d3a83-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3a83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3a83-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3a83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3a83-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a83-106">**Get-AzureRmDiagnosticSetting** cmdlet 'i, kaynak için günlüğe kaydedilen kategorileri ve zaman gratlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d3a83-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="d3a83-107">Zaman aralığı bir ölçümün toplama aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="d3a83-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="d3a83-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3a83-108">EXAMPLES</span></span>

### <span data-ttu-id="d3a83-109">Örnek 1: günlük kategorilerinin ve zaman eklentilerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="d3a83-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="d3a83-110">Bu komut,/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. *RESOURCEID* olan bir Azure Anahtar Kasası için günlüğe kaydedilen kategorileri ve zaman komutlarını alır</span><span class="sxs-lookup"><span data-stu-id="d3a83-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="d3a83-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3a83-111">PARAMETERS</span></span>

### <span data-ttu-id="d3a83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a83-112">-DefaultProfile</span></span>
<span data-ttu-id="d3a83-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d3a83-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3a83-114">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3a83-114">-ResourceId</span></span>
<span data-ttu-id="d3a83-115">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3a83-115">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a83-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a83-116">CommonParameters</span></span>
<span data-ttu-id="d3a83-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3a83-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a83-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a83-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a83-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3a83-119">INPUTS</span></span>

### <span data-ttu-id="d3a83-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3a83-120">None</span></span>
<span data-ttu-id="d3a83-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d3a83-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3a83-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3a83-122">OUTPUTS</span></span>

### <span data-ttu-id="d3a83-123">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="d3a83-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d3a83-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3a83-124">NOTES</span></span>

## <span data-ttu-id="d3a83-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3a83-125">RELATED LINKS</span></span>

[<span data-ttu-id="d3a83-126">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d3a83-126">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


