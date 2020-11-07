---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: eb7dbdee5d1d3d1574be30c5168d97dfcee6ab27
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938875"
---
# <span data-ttu-id="c9dd6-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c9dd6-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="c9dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="c9dd6-103">Günlüğe kaydedilen kategorileri ve zaman grateleri alır.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9dd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9dd6-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9dd6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="c9dd6-106">**Get-AzureRmDiagnosticSetting** cmdlet 'i, kaynak için günlüğe kaydedilen kategorileri ve zaman gratlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="c9dd6-107">Zaman aralığı bir ölçümün toplama aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="c9dd6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9dd6-108">EXAMPLES</span></span>

### <span data-ttu-id="c9dd6-109">Örnek 1: günlük kategorilerinin ve zaman eklentilerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="c9dd6-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="c9dd6-110">Bu komut,/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. *RESOURCEID* olan bir Azure Anahtar Kasası için günlüğe kaydedilen kategorileri ve zaman komutlarını alır</span><span class="sxs-lookup"><span data-stu-id="c9dd6-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="c9dd6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9dd6-111">PARAMETERS</span></span>

### <span data-ttu-id="c9dd6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9dd6-112">-DefaultProfile</span></span>
<span data-ttu-id="c9dd6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c9dd6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9dd6-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9dd6-114">-Name</span></span>
<span data-ttu-id="c9dd6-115">Tanılama ayarının adı.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="c9dd6-116">Verilmezse, önceki API 'da olduğu gibi "hizmet" için çağrı yapın.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-116">If not given the call default to "service" as it was in the previous API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9dd6-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c9dd6-117">-ResourceId</span></span>
<span data-ttu-id="c9dd6-118">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="c9dd6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9dd6-119">CommonParameters</span></span>
<span data-ttu-id="c9dd6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9dd6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9dd6-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9dd6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9dd6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9dd6-122">INPUTS</span></span>

### <span data-ttu-id="c9dd6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c9dd6-123">System.String</span></span>

## <span data-ttu-id="c9dd6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9dd6-124">OUTPUTS</span></span>

### <span data-ttu-id="c9dd6-125">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="c9dd6-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="c9dd6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9dd6-126">NOTES</span></span>

## <span data-ttu-id="c9dd6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9dd6-127">RELATED LINKS</span></span>

<span data-ttu-id="c9dd6-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="c9dd6-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
