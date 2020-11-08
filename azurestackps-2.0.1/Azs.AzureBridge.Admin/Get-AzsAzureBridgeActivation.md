---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2020
ms.locfileid: "94107342"
---
# <span data-ttu-id="f9e44-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="f9e44-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="f9e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e44-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e44-103">Azure Köprüsü etkinleştirme 'yi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9e44-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="f9e44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9e44-104">SYNTAX</span></span>

### <span data-ttu-id="f9e44-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9e44-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f9e44-106">Al</span><span class="sxs-lookup"><span data-stu-id="f9e44-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="f9e44-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f9e44-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f9e44-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9e44-108">DESCRIPTION</span></span>
<span data-ttu-id="f9e44-109">Azure yığını kaydedildikten sonra, etkinleştirme nesnesi Azure 'daki kayda bir Azure yığın dağıtımını bağlayan bilgileri (örneğin, kayıt son kullanım tarihi, ad vb.) içerir.</span><span class="sxs-lookup"><span data-stu-id="f9e44-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="f9e44-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9e44-110">EXAMPLES</span></span>

### <span data-ttu-id="f9e44-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9e44-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="f9e44-112">"ActivationRG" kaynak grubunun altındaki Azure Bridge etkinleştirmeleri listesini alma</span><span class="sxs-lookup"><span data-stu-id="f9e44-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="f9e44-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9e44-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="f9e44-114">' ActivationRG ' altında ' Myacsyon ' adlı bir Azure köprü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f9e44-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="f9e44-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9e44-115">PARAMETERS</span></span>

### <span data-ttu-id="f9e44-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9e44-116">-Name</span></span>
<span data-ttu-id="f9e44-117">Etkinleştirme adı.</span><span class="sxs-lookup"><span data-stu-id="f9e44-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e44-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e44-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9e44-119">Azure yığınının kaydı sırasında kullanılan kaynak grubu; Ayrıca, portalda kaynak grubu adlarını da görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9e44-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e44-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9e44-120">-ResourceId</span></span>
<span data-ttu-id="f9e44-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f9e44-121">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e44-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="f9e44-122">-Skip</span></span>
<span data-ttu-id="f9e44-123">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="f9e44-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e44-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="f9e44-124">-Top</span></span>
<span data-ttu-id="f9e44-125">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="f9e44-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f9e44-126">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f9e44-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9e44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e44-127">CommonParameters</span></span>
<span data-ttu-id="f9e44-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9e44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e44-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e44-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e44-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9e44-130">INPUTS</span></span>

## <span data-ttu-id="f9e44-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9e44-131">OUTPUTS</span></span>

### <span data-ttu-id="f9e44-132">Microsoft. AzureStack. Management. AzureBridge. admin. modeller. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="f9e44-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="f9e44-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9e44-133">NOTES</span></span>

## <span data-ttu-id="f9e44-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9e44-134">RELATED LINKS</span></span>

