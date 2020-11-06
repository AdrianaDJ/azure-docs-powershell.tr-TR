---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2b70fd58bd0b51e03079b1c24665b67ac3ad3a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590252"
---
# <span data-ttu-id="2ccd9-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2ccd9-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="2ccd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ccd9-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccd9-103">Günlüğe kaydedilen kategorileri ve zaman grateleri alır.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ccd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ccd9-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ccd9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ccd9-105">DESCRIPTION</span></span>
<span data-ttu-id="2ccd9-106">**Get-AzureRmDiagnosticSetting** cmdlet 'i, kaynak için günlüğe kaydedilen kategorileri ve zaman gratlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="2ccd9-107">Zaman aralığı bir ölçümün toplama aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="2ccd9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ccd9-108">EXAMPLES</span></span>

### <span data-ttu-id="2ccd9-109">Örnek 1: günlük kategorilerinin ve zaman eklentilerinin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="2ccd9-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="2ccd9-110">Bu komut,/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. *RESOURCEID* olan bir Azure Anahtar Kasası için günlüğe kaydedilen kategorileri ve zaman komutlarını alır</span><span class="sxs-lookup"><span data-stu-id="2ccd9-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="2ccd9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ccd9-111">PARAMETERS</span></span>

### <span data-ttu-id="2ccd9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccd9-112">-DefaultProfile</span></span>
<span data-ttu-id="2ccd9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2ccd9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ccd9-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ccd9-114">-Name</span></span>
<span data-ttu-id="2ccd9-115">Tanılama ayarının adı.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="2ccd9-116">Verilmezse, önceki API 'da olduğu gibi "hizmet" için çağrı yapın.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="2ccd9-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ccd9-117">-ResourceId</span></span>
<span data-ttu-id="2ccd9-118">Kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="2ccd9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccd9-119">CommonParameters</span></span>
<span data-ttu-id="2ccd9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ccd9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccd9-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccd9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccd9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ccd9-122">INPUTS</span></span>

### <span data-ttu-id="2ccd9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2ccd9-123">System.String</span></span>

## <span data-ttu-id="2ccd9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ccd9-124">OUTPUTS</span></span>

### <span data-ttu-id="2ccd9-125">Microsoft. Azure. Commands. Insights. OutputClasses. Psservicedıagnoçıkartma ayarları</span><span class="sxs-lookup"><span data-stu-id="2ccd9-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="2ccd9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ccd9-126">NOTES</span></span>

## <span data-ttu-id="2ccd9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ccd9-127">RELATED LINKS</span></span>

<span data-ttu-id="2ccd9-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd9-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
